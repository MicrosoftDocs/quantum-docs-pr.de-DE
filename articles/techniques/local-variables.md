---
title: 'F #-Techniken-lokale Variablen | Microsoft-Dokumentation'
description: 'F #-Techniken-lokale Variablen'
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 4f5eff1ee8482fa5e5fee9dff421efab93fc0c5a
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/26/2019
ms.locfileid: "73183283"
---
# <a name="local-variables"></a><span data-ttu-id="a0d15-103">Lokale Variablen</span><span class="sxs-lookup"><span data-stu-id="a0d15-103">Local Variables</span></span> #

<span data-ttu-id="a0d15-104">Ein Wert eines beliebigen Typs in Q # kann einer Variablen für die Wiederverwendung innerhalb eines Vorgangs oder einer Funktion mithilfe des `let`-Schlüssel Worts zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="a0d15-104">A value of any type in Q# can be assigned to a variable for reuse within an operation or function by using the `let` keyword.</span></span>
<span data-ttu-id="a0d15-105">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="a0d15-105">For instance:</span></span>

```qsharp
let measurementOperator = [PauliX, PauliZ, PauliZ, PauliX, PauliI];
```

<span data-ttu-id="a0d15-106">Dadurch wird einer Variablen mit dem Namen `measurementOperator`ein bestimmtes Array von Pauli-Operatoren zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="a0d15-106">This assigns a particular array of Pauli operators to a variable called `measurementOperator`.</span></span>

> [!TIP]
> <span data-ttu-id="a0d15-107">Beachten Sie, dass der Typ der neuen Variablen nicht explizit angegeben werden muss, da der Ausdruck auf der rechten Seite der `let` Anweisung eindeutig ist und der Typ vom Compiler abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="a0d15-107">Note that we did not need to explicitly specify the type of our new variable, as the expression on the right-hand side of the `let` statement is unambiguous and the type is inferred by the compiler.</span></span> 

<span data-ttu-id="a0d15-108">Variablen in Q # sind *unveränderlich*. Dies bedeutet, dass eine Variable nicht mehr geändert werden kann, sobald eine Variable auf diese Weise definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a0d15-108">Variables in Q# are *immutable*, meaning that once a variable has been defined in this way, it can no longer be changed in any way.</span></span>
<span data-ttu-id="a0d15-109">Dies ermöglicht eine Reihe nützlicher Optimierungen, einschließlich der Optimierung der klassischen Logik, die auf Variablen angewendet wird, die für die Anwendung der `Adjoint` Variant eines Vorgangs neu angeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="a0d15-109">This allows for several beneficial optimizations, including optimization of the classical logic acting on variables to be reordered for applying the `Adjoint` variant of an operation.</span></span>

<span data-ttu-id="a0d15-110">Variablen, die mit der `let` Bindung wie oben definiert definiert sind, sind für einen bestimmten Bereich lokal, z. b. den Text eines Vorgangs oder den Inhalt einer `for` Schleife.</span><span class="sxs-lookup"><span data-stu-id="a0d15-110">Variables defined using the `let` binding as above are local to a particular scope, such as the body of an operation or the contents of a `for` loop.</span></span>


## <a name="mutability"></a><span data-ttu-id="a0d15-111">Veränderlichkeit</span><span class="sxs-lookup"><span data-stu-id="a0d15-111">Mutability</span></span> ##

<span data-ttu-id="a0d15-112">Als Alternative zum Erstellen einer Variablen mit `let`erstellt das `mutable`-Schlüsselwort eine spezielle änderbare Variable, die nach der anfänglichen Erstellung mithilfe des `set`-Schlüssel Worts erneut gebunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="a0d15-112">As an alternative to creating a variable with `let`, the `mutable` keyword will create a special mutable variable that can be re-bound after it is initially created by using the `set` keyword.</span></span>

```qsharp
operation RandomInts(maxInt : Int, nrSamples : Int) : Int[] {
    mutable samples = new Int[0];
    for (i in 1 .. nrSamples) {
        set samples += [RandomInt(maxInt)];
    }
    return samples;
}
```

<span data-ttu-id="a0d15-113">Alle Typen in Q #, einschließlich Arrays, folgen der Wert Semantik.</span><span class="sxs-lookup"><span data-stu-id="a0d15-113">All types in Q#, including arrays, follow value semantics.</span></span> <span data-ttu-id="a0d15-114">Insbesondere ist es nicht möglich, Array Elemente zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a0d15-114">In particular, it is not possible to update array items.</span></span> <span data-ttu-id="a0d15-115">Wenn Sie ein vorhandenes Array ändern möchten, müssen Sie einen Kopier-und Aktualisierungsmechanismus ähnlich dem für F#Datensätze in nutzen.</span><span class="sxs-lookup"><span data-stu-id="a0d15-115">To modify an existing array requires leveraging a copy-and-update mechanism much like the one for records in F#.</span></span> <span data-ttu-id="a0d15-116">Mithilfe der Bibliotheks Tools für Arrays, die in [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays)bereitgestellt werden, können wir einfach eine Funktion definieren, die ein Array von Paulis zurückgibt, bei dem der Pauli bei Index `i` den angegebenen Wert annimmt und alle anderen Einträge die Identität sind:</span><span class="sxs-lookup"><span data-stu-id="a0d15-116">Using the library tools for arrays provided in [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays), we can e.g. easily define a function that returns an array of Paulis where the Pauli at index `i` takes the given value and all other entries are the identity:</span></span> 

```qsharp
function EmbedPauli (pauli : Pauli, i : Int, n : Int) : Pauli[] {
    
    let arr = ConstantArray(n, PauliI); // creates an array of filled with PauliI
    return arr w/ i <- pauli; // constructs a new array based on arr except that entry i is set to pauli
}
```

<span data-ttu-id="a0d15-117">Weitere Informationen zum Arbeiten mit Arrays finden Sie bei der Erörterung von Q #-Anweisungen und-Ausdrücken.</span><span class="sxs-lookup"><span data-stu-id="a0d15-117">We will elaborate more on how to work with arrays when discussing Q# statements and expressions.</span></span> 

<span data-ttu-id="a0d15-118">Die muability in Q # ist ein Konzept, das für ein *Symbol* anstelle eines Typs oder Werts gilt.</span><span class="sxs-lookup"><span data-stu-id="a0d15-118">Mutability within Q# is a concept that applies to a *symbol* rather than a type or value.</span></span> <span data-ttu-id="a0d15-119">Insbesondere weist Sie weder implizit noch explizit eine Darstellung im Typsystem auf, und ob eine Bindung änderbar (wie durch das `mutable`-Schlüsselwort angegeben) oder unveränderlich (wie durch `let`angegeben) nicht den Typ der gebundenen Variablen ändert.</span><span class="sxs-lookup"><span data-stu-id="a0d15-119">Specifically, it does not have a representation in the type system, implicitly or explicitly, and whether or not a binding is mutable (as indicated by the `mutable` keyword) or immutable (as indicated by `let`) does not change the type of the bound variable(s).</span></span> <span data-ttu-id="a0d15-120">Dies bietet eine wichtige Möglichkeit zum Isolieren der muability in spezialisierten Funktionen und Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="a0d15-120">This provides an important way to isolate mutability inside specialized functions and operations.</span></span>
<span data-ttu-id="a0d15-121">Insbesondere, obwohl eine Adjoint-Spezialisierung für einen Vorgang, der eine änderbare Variable verwendet, nicht automatisch generiert werden kann, funktioniert die automatische Generierung problemlos für einen Vorgang, der eine Funktion aufrufen, die Veränderlichkeit verwendet.</span><span class="sxs-lookup"><span data-stu-id="a0d15-121">In particular, even though an adjoint specialization for an operation which uses a mutable variable cannot be auto-generated, auto-generation works fine for an operation calling a function which uses mutability.</span></span>
<span data-ttu-id="a0d15-122">Aus diesem Grund empfiehlt es sich, Funktionen und Vorgänge zu erstellen, die die Änderbarkeit so kurz und kompakt wie möglich verwenden, sodass der Rest des Quantum-Programms mithilfe normaler unveränderlicher Variablen geschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="a0d15-122">For this reason, it is a good practice to make functions and operations which use mutability as short and compact as possible, so that the rest of the quantum program can be written using ordinary immutable variables.</span></span>


## <a name="deconstruction"></a><span data-ttu-id="a0d15-123">Dekonstruktion</span><span class="sxs-lookup"><span data-stu-id="a0d15-123">Deconstruction</span></span> ##

<span data-ttu-id="a0d15-124">Zusätzlich zum Zuweisen einer einzelnen Variablen ermöglichen die `let`-und `mutable` Schlüsselwörter bzw. ein beliebiges anderes Bindungs Konstrukt auch das Entpacken des Inhalts eines [tupeltyps](xref:microsoft.quantum.language.type-model#tuple-types).</span><span class="sxs-lookup"><span data-stu-id="a0d15-124">In addition to assigning a single variable, the `let` and `mutable` keywords - or in fact any other binding construct - also allow for unpacking the contents of a [tuple type](xref:microsoft.quantum.language.type-model#tuple-types).</span></span>
<span data-ttu-id="a0d15-125">Eine Zuweisung dieses Formulars heißt, dass die Elemente dieses Tupels *deaktiviert* werden.</span><span class="sxs-lookup"><span data-stu-id="a0d15-125">An assignment of this form is said to *deconstruct* the elements of that tuple.</span></span>
<span data-ttu-id="a0d15-126">Wenn wir beispielsweise einen Begriff in einer hamiltona durch ein Tupel modellieren, können wir die Debug-Methode verwenden, um auf die verschiedenen Daten zuzugreifen, die wir unter diesem Begriff simulieren müssen:</span><span class="sxs-lookup"><span data-stu-id="a0d15-126">For instance, if we model a term in a Hamiltonian by a tuple, then we can use deconstruction to access the different data that we need to simulate under that term:</span></span>

```qsharp
// Represents H = 3.1 X_0 Z_1.
let (_, (paulis, idxQubits)) = ((3.1, 1.0), ([PauliX, PauliZ], [0, 1])); // paulis and idxQubits are both immutable variables
mutable ((c1, c2), _) = ((3.1, 1.0), ([PauliX, PauliZ], [0, 1])); // c1 and c2 are both mutable variables
```



---
title: 'Variablen in Q #'
description: füllbeschreibung
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.variables
ms.openlocfilehash: 456c05d4ca66a747e0cc514a30c6bbb33610f481
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "84327780"
---
# <a name="variables-in-q"></a><span data-ttu-id="3342c-103">Variablen in Q #</span><span class="sxs-lookup"><span data-stu-id="3342c-103">Variables in Q#</span></span>

<span data-ttu-id="3342c-104">Q # unterscheidet zwischen veränderbaren und unveränderlichen Symbolen oder "Variables", die an Ausdrücke gebunden/zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="3342c-104">Q# distinguishes between mutable and immutable symbols, or "variables", which are bound/assigned to expressions.</span></span>
<span data-ttu-id="3342c-105">Im Allgemeinen wird die Verwendung unveränderlicher Symbole empfohlen, da es dem Compiler ermöglicht, weitere Optimierungen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="3342c-105">In general, the use of immutable symbols is encouraged because it allows the compiler to perform more optimizations.</span></span>

<span data-ttu-id="3342c-106">Die linke Seite einer Bindung besteht aus einem symboltupel und der rechten Seite eines Ausdrucks.</span><span class="sxs-lookup"><span data-stu-id="3342c-106">The left-hand-side of a binding consists of a symbol tuple, and the right hand side of an expression.</span></span>

## <a name="immutable-variables"></a><span data-ttu-id="3342c-107">Unveränderliche Variablen</span><span class="sxs-lookup"><span data-stu-id="3342c-107">Immutable Variables</span></span>

<span data-ttu-id="3342c-108">Ein Wert eines beliebigen Typs in Q # kann einer Variablen für die Wiederverwendung innerhalb eines Vorgangs oder einer Funktion mithilfe des `let` Schlüssel Worts zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="3342c-108">A value of any type in Q# can be assigned to a variable for reuse within an operation or function by using the `let` keyword.</span></span>

<span data-ttu-id="3342c-109">Eine unveränderliche Bindung besteht aus dem Schlüsselwort `let` , gefolgt von einem Symbol oder einem symboltupel, einem Gleichheitszeichen `=` , einem Ausdruck, an den die Symbole gebunden werden, und einem abschließenden Semikolon.</span><span class="sxs-lookup"><span data-stu-id="3342c-109">An immutable binding consists of the keyword `let`, followed by a symbol or symbol tuple, an equals sign `=`, an expression to bind the symbol(s) to, and a terminating semicolon.</span></span>

<span data-ttu-id="3342c-110">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="3342c-110">For instance:</span></span>

```qsharp
let measurementOperator = [PauliX, PauliZ, PauliZ, PauliX, PauliI];
```

<span data-ttu-id="3342c-111">Dadurch wird dem Variablennamen (oder "Symbol") ein bestimmtes Array von Pauli-Operatoren zugewiesen `measurementOperator` .</span><span class="sxs-lookup"><span data-stu-id="3342c-111">This assigns a particular array of Pauli operators to the variable name (or "symbol"), `measurementOperator`.</span></span>

> [!NOTE]
> <span data-ttu-id="3342c-112">Der Typ der neuen Variablen muss nicht explizit angegeben werden, da der Ausdruck auf der rechten Seite der `let` Anweisung eindeutig ist und der Typ vom Compiler abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="3342c-112">We did not need to explicitly specify the type of our new variable, as the expression on the right-hand side of the `let` statement is unambiguous and the type is inferred by the compiler.</span></span> 

<span data-ttu-id="3342c-113">Mit definierte Variablen `let` sind *unveränderlich*, d. h., nachdem Sie definiert wurde, kann Sie nicht mehr geändert werden.</span><span class="sxs-lookup"><span data-stu-id="3342c-113">Variables defined using `let` are *immutable*, meaning that once it has been defined, it can no longer be changed in any way.</span></span>
<span data-ttu-id="3342c-114">Dies ermöglicht eine Reihe nützlicher Optimierungen, einschließlich der Optimierung der klassischen Logik, die auf Variablen angewendet wird, die für die Anwendung der `Adjoint` Variante eines Vorgangs neu angeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="3342c-114">This allows for several beneficial optimizations, including optimization of the classical logic acting on variables to be reordered for applying the `Adjoint` variant of an operation.</span></span>

## <a name="mutable-variables"></a><span data-ttu-id="3342c-115">Änderbare Variablen</span><span class="sxs-lookup"><span data-stu-id="3342c-115">Mutable Variables</span></span>

<span data-ttu-id="3342c-116">Als Alternative zum Erstellen einer Variablen mit `let` wird mit dem- `mutable` Schlüsselwort eine änderbare Variable erstellt, die nach der anfänglichen Erstellung mithilfe des Schlüssel Worts erneut gebunden werden *kann* `set` .</span><span class="sxs-lookup"><span data-stu-id="3342c-116">As an alternative to creating a variable with `let`, the `mutable` keyword will create a mutable variable that *can* be re-bound after it is initially created by using the `set` keyword.</span></span>

<span data-ttu-id="3342c-117">Symbole, die als Teil einer-Anweisung deklariert und gebunden `mutable` werden, können später im Code an einen anderen Wert zurückgebunden werden.</span><span class="sxs-lookup"><span data-stu-id="3342c-117">Symbols declared and bound as part of a `mutable` statement may be rebound to a different value later in the code.</span></span> <span data-ttu-id="3342c-118">Wenn ein Symbol später im Code wieder verwendet wird, wird der Typ nicht geändert, und der neu gebundene Wert muss mit diesem Typ kompatibel sein.</span><span class="sxs-lookup"><span data-stu-id="3342c-118">If a symbol is rebound later in the code, its type does not change, and the newly bound value needs to be compatible with that type.</span></span>

### <a name="rebinding-of-mutable-symbols"></a><span data-ttu-id="3342c-119">Neubinden von änderbaren Symbolen</span><span class="sxs-lookup"><span data-stu-id="3342c-119">Rebinding of Mutable Symbols</span></span>

<span data-ttu-id="3342c-120">Eine änderbare Variable kann mit einer-Anweisung wieder verwendet werden `set` .</span><span class="sxs-lookup"><span data-stu-id="3342c-120">A mutable variable may be rebound using a `set` statement.</span></span>
<span data-ttu-id="3342c-121">Eine solche erneute Bindung besteht aus dem Schlüsselwort `set` , gefolgt von einem Symbol oder einem symboltupel, einem Gleichheitszeichen `=` , einem Ausdruck zum erneuten Binden der Symbole an und einem abschließenden Semikolon.</span><span class="sxs-lookup"><span data-stu-id="3342c-121">Such a rebinding consists of the keyword `set`, followed by a symbol or symbol tuple, an equals sign `=`, an expression to rebind the symbol(s) to, and a terminating semicolon.</span></span>

<span data-ttu-id="3342c-122">Hier finden Sie einige Beispiele für Methoden zur Neubindung von Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="3342c-122">Here, we provide some possible examples of rebinding statement techniques</span></span>

### <a name="apply-and-reassign-statements"></a><span data-ttu-id="3342c-123">Apply-and-REASSIGN-Anweisungen</span><span class="sxs-lookup"><span data-stu-id="3342c-123">Apply-and-Reassign Statements</span></span>

<span data-ttu-id="3342c-124">Eine bestimmte Art von `set` -Anweisung, auf die als *Apply-and-REASSIGN* -Anweisung verwiesen wird, stellt eine bequeme Methode für die Verkettung dar, wenn die Rechte Seite aus der Anwendung eines binären Operators besteht und das Ergebnis an das linke Argument des Operators gebunden werden soll.</span><span class="sxs-lookup"><span data-stu-id="3342c-124">A particular kind of `set`-statement we refer to as an *apply-and-reassign* statement provides a convenient way of concatenation if the right hand side consists of the application of a binary operator and the result is to be rebound to the left argument to the operator.</span></span> <span data-ttu-id="3342c-125">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="3342c-125">For example,</span></span>
```qsharp
mutable counter = 0;
for (i in 1 .. 2 .. 10) {
    set counter += 1;
    // ...
}
```
<span data-ttu-id="3342c-126">Inkremente `counter` in jeder Iterations Schleife den Wert des Zählers `for` .</span><span class="sxs-lookup"><span data-stu-id="3342c-126">increments the value of the counter `counter` in each iteration of the `for` loop.</span></span> <span data-ttu-id="3342c-127">Der obige Code entspricht</span><span class="sxs-lookup"><span data-stu-id="3342c-127">The code above is equivalent to</span></span> 
```qsharp
mutable counter = 0;
for (i in 1 .. 2 .. 10) {
    set counter = counter + 1;
    // ...
}
```

<span data-ttu-id="3342c-128">Ähnliche Anweisungen sind für alle binären Operatoren verfügbar, in denen der Typ der linken Seite mit dem Ausdruckstyp übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="3342c-128">Similar statements are available for all binary operators in which the type of the left-hand-side matches the expression type.</span></span> <span data-ttu-id="3342c-129">Dies stellt beispielsweise eine bequeme Möglichkeit zum Sammeln von Werten dar.</span><span class="sxs-lookup"><span data-stu-id="3342c-129">This provides for example a convenient way to accumulate values.</span></span>

<span data-ttu-id="3342c-130">Beispielsweise ist "supposiposiposiposiposiposiposiposiposierend" `qubits` ein regsiter</span><span class="sxs-lookup"><span data-stu-id="3342c-130">For example, supposing `qubits` is a regsiter of qubits:</span></span>
```qsharp
mutable results = new Result[0];   // results is an empty array of type Result[]
for (q in qubits) {
    set results += [M(q)];         // concatenate the outcome from measuring q to the existing array
    // ...
}
...                                // results contains the measurement outcomes from the whole register
```

### <a name="update-and-reassign-statements"></a><span data-ttu-id="3342c-131">Update-und-REASSIGN-Anweisungen</span><span class="sxs-lookup"><span data-stu-id="3342c-131">Update-and-Reassign Statements</span></span>

<span data-ttu-id="3342c-132">Eine ähnliche Verkettung ist für [Kopier-und Update Ausdrücke](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions) auf der rechten Seite vorhanden.</span><span class="sxs-lookup"><span data-stu-id="3342c-132">A similar concatenation exists for [copy-and-update expressions](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions) on the right-hand-side.</span></span>
<span data-ttu-id="3342c-133">Entsprechend sind *Update-und-REASSIGN* -Anweisungen für *benannte Elemente* in benutzerdefinierten Typen sowie für *Array Elemente*vorhanden.</span><span class="sxs-lookup"><span data-stu-id="3342c-133">Correspondingly, *update-and-reassign* statements exist for *named items* in user-defined types as well as for *array items*.</span></span>  

```qsharp
newtype Complex = (Re : Double, Im : Double);

function ComplexSum(reals : Double[], ims : Double[]) : Complex[] {
    mutable res = Complex(0.,0.);

    for (r in reals) {
        set res w/= Re <- res::Re + r; // update-and-reassign statement
    }
    for (i in ims) {
        set res w/= Im <- res::Im + i; // update-and-reassign statement
    }
    return res;
}
```

<span data-ttu-id="3342c-134">Im Fall von Arrays [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) stellt in unseren Standardbibliotheken die erforderlichen Tools für viele gängige Anforderungen an die Initialisierung und Bearbeitung von Arrays bereit, sodass es nicht erforderlich ist, Array Elemente an erster Stelle zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="3342c-134">In the case of arrays, [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) in our standard libraries provides the necessary tools for many common array initialization and manipulation needs, and thus help avoid having to update array items in the first place.</span></span> 

<span data-ttu-id="3342c-135">Update-und-REASSIGN-Anweisungen stellen bei Bedarf eine Alternative dar:</span><span class="sxs-lookup"><span data-stu-id="3342c-135">Update-and-reassign statements provide an alternative if needed:</span></span>

```qsharp
operation GenerateRandomInts(max : Int, nSamples : Int) : Int[] {
    mutable samples = new Double[0];
    for (i in 1 .. nSamples) {
        set samples += [RandomInt(max)];
    }
    return samples;
}

operation SampleUniformDistrbution(nSamples : Int, nSteps : Int) : Double[] {
    let normalization = 1. / IntAsDouble(nSteps);
    mutable samples = GenerateRandomInts(nSteps, nSamples);
    
    for (i in IndexRange(samples) {
        let value = IntAsDouble(samples[i]);
        set samples w/= i <- normalization * value; // update-and-reassign statement
    }
}

```

<span data-ttu-id="3342c-136">Mithilfe der Bibliotheks Tools für Arrays, die in bereitgestellt werden, können Sie z. b. [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) einfach eine Funktion definieren, die ein Array von "Paulis" zurückgibt, bei dem der Pauli bei Index `i` den angegebenen Wert annimmt und alle anderen Einträge die Identität sind.</span><span class="sxs-lookup"><span data-stu-id="3342c-136">Using the library tools for arrays provided in [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays), we can, for example, easily define a function that returns an array of Paulis where the Pauli at index `i` takes the given value and all other entries are the identity.</span></span>

<span data-ttu-id="3342c-137">Im folgenden finden Sie zwei Definitionen einer solchen Funktion, wobei die zweite die von Ihnen zur Verfügung stehenden Tools nutzt.</span><span class="sxs-lookup"><span data-stu-id="3342c-137">Here are two definitions of such a function, with the second taking advantage of the tools at our disposal.</span></span>

```qsharp
function PauliEmbedding(pauli : Pauli, length : Int, location : Int) : Pauli[] {
    mutable pauliArray = new Pauli[length];             // initialize pauliArray of given length
    for (index in 0 .. length - 1) {                    // iterate over the integers in the length range
        set pauliArray w/= index <-                     // change the value at index to input pauli or PauliI
            index == location ? pauli | PauliI;         // cond. expression evaluating to pauli or PauliI dep. on whether index==location
    }    
    return pauliArray;
}
```

<span data-ttu-id="3342c-138">Anstatt jeden Index im Array zu durchlaufen und ihn bedingt auf oder festzulegen `PauliI` `Pauli` , können wir stattdessen aus verwenden, `ConstantArray` [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) um ein Array von zu erstellen `PauliI` , und dann einfach einen Copy-and-Update-Ausdruck zurückgeben, in dem wir den bestimmter-Wert bei Index geändert haben `location` :</span><span class="sxs-lookup"><span data-stu-id="3342c-138">Instead of iterating over each index in the array, and conditionally setting it to `PauliI` or `Pauli`, we can instead use `ConstantArray` from [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) to create an array of `PauliI`'s, and then simply returning a copy-and-update expression in which we've changed the specifc value at index `location`:</span></span>

```qsharp
function PauliEmbedding(pauli : Pauli, length : Int, location : Int) : Pauli[] {
    return ConstantArray(length, PauliI) w/ location <- pauli;
}
```

## <a name="tuple-deconstruction"></a><span data-ttu-id="3342c-139">Tupelerstellung</span><span class="sxs-lookup"><span data-stu-id="3342c-139">Tuple Deconstruction</span></span>

<span data-ttu-id="3342c-140">Zusätzlich zum Zuweisen einer einzelnen Variablen werden die `let` `mutable` Schlüsselwörter und---oder tatsächlich jedes andere Bindungs Konstrukt, wie z. b. `set` (unten beschrieben),---auch das Entpacken des Inhalts eines [tupeltyps](xref:microsoft.quantum.guide.types#tuple-types)ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="3342c-140">In addition to assigning a single variable, the `let` and `mutable` keywords---or in fact any other binding construct, such as `set` (described below)---also allow for unpacking the contents of a [tuple type](xref:microsoft.quantum.guide.types#tuple-types).</span></span>
<span data-ttu-id="3342c-141">Eine Zuweisung dieses Formulars heißt, dass die Elemente dieses Tupels *deaktiviert* werden.</span><span class="sxs-lookup"><span data-stu-id="3342c-141">An assignment of this form is said to *deconstruct* the elements of that tuple.</span></span>

<span data-ttu-id="3342c-142">Wenn die Rechte Seite der Bindung ein Tupel ist, kann dieses Tupel bei der Zuweisung dekonstruiert werden.</span><span class="sxs-lookup"><span data-stu-id="3342c-142">If the right-hand side of the binding is a tuple, then that tuple may be deconstructed upon assignment.</span></span>
<span data-ttu-id="3342c-143">Solche Dekonstruktionen können geschaltete Tupel einschließen, und jede vollständige oder partielle Dekonstruktion ist gültig, solange die Form des Tupels auf der rechten Seite mit der Form des symboltupels kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="3342c-143">Such deconstructions may involve nested tuples, and any full or partial deconstruction is valid as long as the shape of the tuple on the right hand side is compatible with the shape of the symbol tuple.</span></span>

<span data-ttu-id="3342c-144">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="3342c-144">For example:</span></span>

```qsharp
let (i, f) = (5, 0.1); // i is bound to 5 and f to 0.1
mutable (a, (_, b)) = (1, (2, 3)); // a is bound to 1, b is bound to 3
mutable (x, y) = ((1, 2), [3, 4]); // x is bound to (1,2), y is bound to [3,4]
set (x, _, y) = ((5, 6), 7, [8]);  // x is rebound to (5,6), y is rebound to [8]
let (r1, r2) = MeasureTwice(q1, PauliX, q2, PauliY);
```

## <a name="binding-scopes"></a><span data-ttu-id="3342c-145">Bindungs Bereiche</span><span class="sxs-lookup"><span data-stu-id="3342c-145">Binding Scopes</span></span>

<span data-ttu-id="3342c-146">Im allgemeinen verlassen Symbol Bindungen den Gültigkeitsbereich und werden am Ende des Anweisungsblocks, in dem Sie auftreten, inaktiv.</span><span class="sxs-lookup"><span data-stu-id="3342c-146">In general, symbol bindings go out of scope and become inoperative at the end of the statement block they occur in.</span></span>
<span data-ttu-id="3342c-147">Es gibt jedoch zwei Ausnahmen:</span><span class="sxs-lookup"><span data-stu-id="3342c-147">There are two exceptions to this rule:</span></span>

- <span data-ttu-id="3342c-148">Die Bindung der Schleifen Variablen einer Schleife liegt im Gültigkeitsbereich des Texts der `for` for-Schleife, aber nicht nach dem Ende der Schleife.</span><span class="sxs-lookup"><span data-stu-id="3342c-148">The binding of the loop variable of a `for` loop is in scope for the body of the for loop, but not after the end of the loop.</span></span>
- <span data-ttu-id="3342c-149">Alle drei Teile einer `repeat` / `until` Schleife (der Text, der Test und das Fixup) werden als einzelner Bereich behandelt, sodass im Text gebundene Symbole im Test und im Fixup verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="3342c-149">All three portions of a `repeat`/`until` loop (the body, the test, and the fixup) are treated as a single scope, so symbols that are bound in the body are available in the test and in the fixup.</span></span>

<span data-ttu-id="3342c-150">Für beide Schleifen Typen wird jeder Durchlauf der Schleife in einem eigenen Bereich ausgeführt, sodass Bindungen aus einem früheren Durchlauf in einem späteren Durchlauf nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="3342c-150">For both types of loops, each pass through the loop executes in its own scope, so bindings from an earlier pass are not available in a later pass.</span></span>
<span data-ttu-id="3342c-151">Details zu diesen Schleifen finden Sie unter [Ablauf Steuerung](xref:microsoft.quantum.guide.controlflow).</span><span class="sxs-lookup"><span data-stu-id="3342c-151">Details on these loops can be found at [Control Flow](xref:microsoft.quantum.guide.controlflow).</span></span>

<span data-ttu-id="3342c-152">Symbol Bindungen aus äußeren Blöcken werden von inneren Blöcken geerbt.</span><span class="sxs-lookup"><span data-stu-id="3342c-152">Symbol bindings from outer blocks are inherited by inner blocks.</span></span>
<span data-ttu-id="3342c-153">Ein Symbol kann nur einmal pro Block gebunden werden. Es ist unzulässig, ein Symbol mit dem gleichen Namen wie ein anderes Symbol zu definieren, das sich im Gültigkeitsbereich befindet (kein "shadodown").</span><span class="sxs-lookup"><span data-stu-id="3342c-153">A symbol may only be bound once per block; it is illegal to define a symbol with the same name as another symbol that is within scope (no "shadowing").</span></span>
<span data-ttu-id="3342c-154">Die folgenden Sequenzen sind zulässig:</span><span class="sxs-lookup"><span data-stu-id="3342c-154">The following sequences would be legal:</span></span>

```qsharp
if (a == b) {
    ...
    let n = 5;
    ...             // n is 5
}
let n = 8;
...                 // n is 8
```

<span data-ttu-id="3342c-155">and</span><span class="sxs-lookup"><span data-stu-id="3342c-155">and</span></span>

```qsharp
if (a == b) {
    ...
    let n = 5;
    ...             // n is 5
} else {
    ...
    let n = 8;
    ...             // n is 8
}
...                 // n is not bound to a value
```

<span data-ttu-id="3342c-156">Dies wäre jedoch unzulässig:</span><span class="sxs-lookup"><span data-stu-id="3342c-156">But this would be illegal:</span></span>

```qsharp
let n = 5;
...                 // n is 5
let n = 8;          // Error!!
...
```

<span data-ttu-id="3342c-157">wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3342c-157">as would:</span></span>

```qsharp
let n = 8;
if (a == b) {
    ...             // n is 8
    let n = 5;      // Error!
    ...
}
...
```

## <a name="next-steps"></a><span data-ttu-id="3342c-158">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="3342c-158">Next steps</span></span>

<span data-ttu-id="3342c-159">Erfahren Sie mehr über das [Arbeiten mit Qubits](xref:microsoft.quantum.guide.qubits) in f #.</span><span class="sxs-lookup"><span data-stu-id="3342c-159">Learn about [Working With Qubits](xref:microsoft.quantum.guide.qubits) in Q#.</span></span>
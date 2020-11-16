---
title: 'Variablen in Q#'
description: 'Erfahren Sie, wie Sie mit verschiedenen Variablen in arbeiten können. Q#'
author: gillenhaalb
ms.author: a-gibec
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.variables
no-loc:
- 'Q#'
- '$$v'
ms.openlocfilehash: 67c71c09e004d77360902360fefc7a7752e4a829
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92690937"
---
# <a name="variables-in-no-locq"></a><span data-ttu-id="546fe-103">Variablen in Q#</span><span class="sxs-lookup"><span data-stu-id="546fe-103">Variables in Q#</span></span>

<span data-ttu-id="546fe-104">Q# unterscheidet zwischen veränderbaren und unveränderlichen Symbolen oder *Variablen* , die an Ausdrücke gebunden/zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="546fe-104">Q# distinguishes between mutable and immutable symbols, or *variables* , which are bound/assigned to expressions.</span></span>
<span data-ttu-id="546fe-105">Im Allgemeinen wird die Verwendung unveränderlicher Symbole empfohlen, da es dem Compiler ermöglicht, weitere Optimierungen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="546fe-105">In general, the use of immutable symbols is encouraged because it allows the compiler to perform more optimizations.</span></span>

<span data-ttu-id="546fe-106">Die linke Seite einer Bindung besteht aus einem symboltupel und der rechten Seite eines Ausdrucks.</span><span class="sxs-lookup"><span data-stu-id="546fe-106">The left-hand-side of a binding consists of a symbol tuple and the right-hand side of an expression.</span></span>

## <a name="immutable-variables"></a><span data-ttu-id="546fe-107">Unveränderliche Variablen</span><span class="sxs-lookup"><span data-stu-id="546fe-107">Immutable Variables</span></span>

<span data-ttu-id="546fe-108">Sie können einen Wert eines beliebigen Typs in Q# einer Variablen für die Wiederverwendung innerhalb eines Vorgangs oder einer Funktion mithilfe des `let` Schlüssel Worts zuweisen.</span><span class="sxs-lookup"><span data-stu-id="546fe-108">You can assign a value of any type in Q# to a variable for reuse within an operation or function by using the `let` keyword.</span></span> 

<span data-ttu-id="546fe-109">Eine unveränderliche Bindung besteht aus dem Schlüsselwort `let` , gefolgt von einem Symbol oder einem symboltupel, einem Gleichheitszeichen `=` , einem Ausdruck, an den die Symbole gebunden werden, und einem abschließenden Semikolon.</span><span class="sxs-lookup"><span data-stu-id="546fe-109">An immutable binding consists of the keyword `let`, followed by a symbol or symbol tuple, an equals sign `=`, an expression to bind the symbol(s) to, and a terminating semicolon.</span></span>

<span data-ttu-id="546fe-110">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="546fe-110">For instance:</span></span>

```qsharp
let measurementOperator = [PauliX, PauliZ, PauliZ, PauliX, PauliI];
```

<span data-ttu-id="546fe-111">Dadurch wird dem Variablennamen (oder "Symbol") ein bestimmtes Array von Pauli-Operatoren zugewiesen `measurementOperator` .</span><span class="sxs-lookup"><span data-stu-id="546fe-111">This assigns a particular array of Pauli operators to the variable name (or "symbol"), `measurementOperator`.</span></span>

> [!NOTE]
> <span data-ttu-id="546fe-112">Im vorherigen Beispiel muss der Typ der neuen Variablen nicht explizit angegeben werden, da der Ausdruck auf der rechten Seite der `let` Anweisung eindeutig ist, und der Compiler leitet den richtigen Typ ab.</span><span class="sxs-lookup"><span data-stu-id="546fe-112">In the previous example, there is no need to explicitly specify the type of the new variable, as the expression on the right-hand side of the `let` statement is unambiguous, and the compiler infers the correct type.</span></span> 

<span data-ttu-id="546fe-113">Variablen `let` , die mit definiert werden, sind *unveränderlich* . Dies bedeutet, dass Sie nach der Definition nicht mehr in irgendeiner Weise geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="546fe-113">Variables defined using `let` are *immutable* , meaning that once you define it, you can no longer change it in any way.</span></span>
<span data-ttu-id="546fe-114">Dies ermöglicht eine Reihe nützlicher Optimierungen, einschließlich der Optimierung der klassischen Logik, die für die Neuanordnung von Variablen zum Anwenden der `Adjoint` Variante eines Vorgangs durchgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="546fe-114">This allows for several beneficial optimizations, including optimization of the classical logic that acts on variables to be reordered for applying the `Adjoint` variant of an operation.</span></span>

## <a name="mutable-variables"></a><span data-ttu-id="546fe-115">Änderbare Variablen</span><span class="sxs-lookup"><span data-stu-id="546fe-115">Mutable Variables</span></span>

<span data-ttu-id="546fe-116">Als Alternative zum Erstellen einer Variablen mit `let` erstellt das- `mutable` Schlüsselwort eine änderbare Variable, die nach der anfänglichen Erstellung mithilfe des-Schlüssel Worts wieder hergestellt werden *kann* `set` .</span><span class="sxs-lookup"><span data-stu-id="546fe-116">As an alternative to creating a variable with `let`, the `mutable` keyword creates a mutable variable that *can* be rebound after it is initially created by using the `set` keyword.</span></span>

<span data-ttu-id="546fe-117">Sie können Symbole, die als Teil einer Anweisung deklariert und als Teil einer Anweisung gebunden wurden `mutable` , an einen anderen Wert weiter unten im Code binden.</span><span class="sxs-lookup"><span data-stu-id="546fe-117">You can rebind symbols declared and bound as part of a `mutable` statement to a different value later in the code.</span></span> <span data-ttu-id="546fe-118">Wenn ein Symbol später im Code wieder verwendet wird, wird der Typ nicht geändert, und der neu gebundene Wert muss mit diesem Typ kompatibel sein.</span><span class="sxs-lookup"><span data-stu-id="546fe-118">If a symbol is rebound later in the code, its type does not change, and the newly bound value must be compatible with that type.</span></span>

### <a name="rebinding-of-mutable-symbols"></a><span data-ttu-id="546fe-119">Neubinden von änderbaren Symbolen</span><span class="sxs-lookup"><span data-stu-id="546fe-119">Rebinding of Mutable Symbols</span></span>

<span data-ttu-id="546fe-120">Sie können eine änderbare Variable mithilfe einer-Anweisung erneut binden `set` .</span><span class="sxs-lookup"><span data-stu-id="546fe-120">You can rebind a mutable variable using a `set` statement.</span></span>
<span data-ttu-id="546fe-121">Eine solche erneute Bindung besteht aus dem Schlüsselwort `set` , gefolgt von einem Symbol oder einem symboltupel, einem Gleichheitszeichen `=` , einem Ausdruck zum erneuten Binden der Symbole an und einem abschließenden Semikolon.</span><span class="sxs-lookup"><span data-stu-id="546fe-121">Such a rebinding consists of the keyword `set`, followed by a symbol or symbol tuple, an equals sign `=`, an expression to rebind the symbol(s) to, and a terminating semicolon.</span></span>

<span data-ttu-id="546fe-122">Im folgenden finden Sie einige Beispiele für Methoden zur Neubindung von Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="546fe-122">The following are some examples of rebinding statement techniques.</span></span>

#### <a name="apply-and-reassign-statements"></a><span data-ttu-id="546fe-123">Apply-and-REASSIGN-Anweisungen</span><span class="sxs-lookup"><span data-stu-id="546fe-123">Apply-and-Reassign Statements</span></span>

<span data-ttu-id="546fe-124">Eine bestimmte Art von `set` -Anweisung, die *Apply-and-REASSIGN* -Anweisung, stellt eine bequeme Möglichkeit zur Verkettung dar, wenn die Rechte Seite aus der Anwendung eines binären Operators besteht und das Ergebnis an das linke Argument des Operators zurückgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="546fe-124">A particular kind of `set`-statement, the *apply-and-reassign* statement, provides a convenient way of concatenation if the right-hand side consists of the application of a binary operator, and the result is to be rebound to the left argument to the operator.</span></span> <span data-ttu-id="546fe-125">Ein auf ein Objekt angewendeter</span><span class="sxs-lookup"><span data-stu-id="546fe-125">For example,</span></span>

```qsharp
mutable counter = 0;
for (i in 1 .. 2 .. 10) {
    set counter += 1;
    // ...
}
```
<span data-ttu-id="546fe-126">Inkremente `counter` in jeder Iterations Schleife den Wert des Zählers `for` .</span><span class="sxs-lookup"><span data-stu-id="546fe-126">increments the value of the counter `counter` in each iteration of the `for` loop.</span></span> <span data-ttu-id="546fe-127">Der vorherige Code entspricht.</span><span class="sxs-lookup"><span data-stu-id="546fe-127">The previous code is equivalent to</span></span> 

```qsharp
mutable counter = 0;
for (i in 1 .. 2 .. 10) {
    set counter = counter + 1;
    // ...
}
```

<span data-ttu-id="546fe-128">Ähnliche Anweisungen sind für alle binären Operatoren verfügbar, in denen der Typ der linken Seite mit dem Ausdruckstyp übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="546fe-128">Similar statements are available for all binary operators in which the type of the left-hand side matches the expression type.</span></span> <span data-ttu-id="546fe-129">Diese Anweisungen stellen eine bequeme Möglichkeit zum Sammeln von Werten dar.</span><span class="sxs-lookup"><span data-stu-id="546fe-129">These statements provide a convenient way to accumulate values.</span></span>

<span data-ttu-id="546fe-130">Beispielsweise ist die Untersetzung `qubits` ein Register von Qubits:</span><span class="sxs-lookup"><span data-stu-id="546fe-130">For example, supposing `qubits` is a register of qubits:</span></span>
```qsharp
mutable results = new Result[0];   // results is an empty array of type Result[]
for (q in qubits) {
    set results += [M(q)];         // concatenate the outcome from measuring q to the existing array
    // ...
}
...                                // results contains the measurement outcomes from the whole register
```

#### <a name="update-and-reassign-statements"></a><span data-ttu-id="546fe-131">Update-und-REASSIGN-Anweisungen</span><span class="sxs-lookup"><span data-stu-id="546fe-131">Update-and-Reassign Statements</span></span>

<span data-ttu-id="546fe-132">Eine ähnliche Verkettung ist für [Copy-und Update-Ausdrücke](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions) auf der rechten Seite vorhanden.</span><span class="sxs-lookup"><span data-stu-id="546fe-132">A similar concatenation exists for [copy-and-update expressions](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions) on the right-hand side.</span></span>
<span data-ttu-id="546fe-133">Entsprechend sind *Update-und-REASSIGN* -Anweisungen für *benannte Elemente* in benutzerdefinierten Typen sowie für *Array Elemente* vorhanden.</span><span class="sxs-lookup"><span data-stu-id="546fe-133">Correspondingly, *update-and-reassign* statements exist for *named items* in user-defined types as well as for *array items* .</span></span>  

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

<span data-ttu-id="546fe-134">Im Fall von Arrays [`Microsoft.Quantum.Arrays`](xref:Microsoft.Quantum.Arrays) stellt in der Q# Standardbibliothek die erforderlichen Tools für viele gängige Anforderungen an die Initialisierung und Bearbeitung von Arrays bereit, sodass es nicht erforderlich ist, Array Elemente an erster Stelle zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="546fe-134">In the case of arrays, [`Microsoft.Quantum.Arrays`](xref:Microsoft.Quantum.Arrays) in the Q# standard library provides the necessary tools for many common array initialization and manipulation needs, and thus helps avoid having to update array items in the first place.</span></span> 

<span data-ttu-id="546fe-135">Update-und-REASSIGN-Anweisungen stellen bei Bedarf eine Alternative dar:</span><span class="sxs-lookup"><span data-stu-id="546fe-135">Update-and-reassign statements provide an alternative if needed:</span></span>

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

<span data-ttu-id="546fe-136">Mithilfe der Bibliotheks Tools für Arrays, die in bereitgestellt werden, [`Microsoft.Quantum.Arrays`](xref:Microsoft.Quantum.Arrays) können Sie z. b. problemlos eine Funktion definieren, die ein Array von Typen zurückgibt, `Pauli` wobei das Element bei Index `i` einen bestimmten `Pauli` Wert annimmt und alle anderen Einträge die Identität ( `PauliI` ) sind.</span><span class="sxs-lookup"><span data-stu-id="546fe-136">Using the library tools for arrays provided in [`Microsoft.Quantum.Arrays`](xref:Microsoft.Quantum.Arrays), you can, for example, easily define a function that returns an array of `Pauli` types where the element at index `i` takes a given `Pauli` value, and all other entries are the identity (`PauliI`).</span></span>

<span data-ttu-id="546fe-137">Im folgenden finden Sie zwei Definitionen einer solchen Funktion, wobei die zweite die von Ihnen zur Verfügung stehenden Tools nutzt.</span><span class="sxs-lookup"><span data-stu-id="546fe-137">Here are two definitions of such a function, with the second taking advantage of the tools at our disposal.</span></span>

```qsharp
function PauliEmbedding(pauli : Pauli, length : Int, location : Int) : Pauli[] {
    mutable pauliArray = new Pauli[length];             // initialize pauliArray of given length
    for (index in 0 .. length - 1) {                    // iterate over the integers in the length range
        set pauliArray w/= index <-                     // change the value at index to input pauli or PauliI
            index == location ? pauli | PauliI;         // cond. expression evaluating to pauli if index==location and PauliI if not
    }    
    return pauliArray;
}
```

<span data-ttu-id="546fe-138">Anstatt jeden Index im Array zu durchlaufen und ihn bedingt auf `PauliI` oder das angegebene festzulegen `pauli` , können Sie stattdessen in verwenden, `ConstantArray` [`Microsoft.Quantum.Arrays`](xref:Microsoft.Quantum.Arrays) um ein Array von Typen zu erstellen `PauliI` , und dann einfach einen Copy-and-Update-Ausdruck zurückgeben, in dem Sie den spezifischen Wert bei Index geändert haben `location` :</span><span class="sxs-lookup"><span data-stu-id="546fe-138">Instead of iterating over each index in the array, and conditionally setting it to `PauliI` or the given `pauli`, you can instead use `ConstantArray` from [`Microsoft.Quantum.Arrays`](xref:Microsoft.Quantum.Arrays) to create an array of `PauliI` types, and then simply return a copy-and-update expression in which you've changed the specific value at index `location`:</span></span>

```qsharp
function PauliEmbedding(pauli : Pauli, length : Int, location : Int) : Pauli[] {
    return ConstantArray(length, PauliI) w/ location <- pauli;
}
```

## <a name="tuple-deconstruction"></a><span data-ttu-id="546fe-139">Tupelerstellung</span><span class="sxs-lookup"><span data-stu-id="546fe-139">Tuple Deconstruction</span></span>

<span data-ttu-id="546fe-140">Zusätzlich zum Zuweisen einer einzelnen Variablen können Sie die `let` `mutable` Schlüsselwörter und oder ein beliebiges anderes Bindungs Konstrukt verwenden, z `set` . b., um den Inhalt eines [tupeltyps](xref:microsoft.quantum.guide.types#tuple-types)zu entpacken.</span><span class="sxs-lookup"><span data-stu-id="546fe-140">In addition to assigning a single variable, you can use the `let` and `mutable` keywords - or any other binding construct, such as `set` - to unpack the contents of a [tuple type](xref:microsoft.quantum.guide.types#tuple-types).</span></span>
<span data-ttu-id="546fe-141">Eine Zuweisung dieses Formulars heißt, dass die Elemente dieses Tupels *deaktiviert* werden.</span><span class="sxs-lookup"><span data-stu-id="546fe-141">An assignment of this form is said to *deconstruct* the elements of that tuple.</span></span>

<span data-ttu-id="546fe-142">Wenn die Rechte Seite der Bindung ein Tupel ist, können Sie dieses Tupel bei der Zuweisung dekonstruieren.</span><span class="sxs-lookup"><span data-stu-id="546fe-142">If the right-hand side of the binding is a tuple, then you can deconstruct that tuple upon assignment.</span></span>
<span data-ttu-id="546fe-143">Solche Dekonstruktionen können geschaltete Tupel einschließen, und jede vollständige oder partielle Dekonstruktion ist gültig, solange die Form des Tupels auf der rechten Seite mit der Form des symboltupels kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="546fe-143">Such deconstructions can involve nested tuples, and any full or partial deconstruction is valid as long as the shape of the tuple on the right-hand side is compatible with the shape of the symbol tuple.</span></span>

<span data-ttu-id="546fe-144">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="546fe-144">For example:</span></span>

```qsharp
let (i, f) = (5, 0.1); // i is bound to 5 and f to 0.1
mutable (a, (_, b)) = (1, (2, 3)); // a is bound to 1, b is bound to 3
mutable (x, y) = ((1, 2), [3, 4]); // x is bound to (1,2), y is bound to [3,4]
set (x, _, y) = ((5, 6), 7, [8]);  // x is rebound to (5,6), y is rebound to [8]
let (r1, r2) = MeasureTwice(q1, PauliX, q2, PauliY);
```

## <a name="binding-scopes"></a><span data-ttu-id="546fe-145">Bindungs Bereiche</span><span class="sxs-lookup"><span data-stu-id="546fe-145">Binding Scopes</span></span>

<span data-ttu-id="546fe-146">Im allgemeinen verlassen Symbol Bindungen den Gültigkeitsbereich und werden am Ende des Anweisungsblocks, in dem Sie auftreten, inaktiv.</span><span class="sxs-lookup"><span data-stu-id="546fe-146">In general, symbol bindings go out of scope and become inoperative at the end of the statement block they occur in.</span></span>
<span data-ttu-id="546fe-147">Es gibt jedoch zwei Ausnahmen:</span><span class="sxs-lookup"><span data-stu-id="546fe-147">There are two exceptions to this rule:</span></span>

- <span data-ttu-id="546fe-148">Die Bindung der Schleifen Variablen einer Schleife liegt im Gültigkeitsbereich des Texts der `for` for-Schleife, aber nicht nach dem Ende der Schleife.</span><span class="sxs-lookup"><span data-stu-id="546fe-148">The binding of the loop variable of a `for` loop is in scope for the body of the for loop, but not after the end of the loop.</span></span>
- <span data-ttu-id="546fe-149">Alle drei Teile einer `repeat` / `until` Schleife (der Text, der Test und das Fixup) fungieren als einzelner Bereich, sodass im Text gebundene Symbole im Test und im Fixup verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="546fe-149">All three portions of a `repeat`/`until` loop (the body, the test, and the fixup) act as a single scope, so symbols that are bound in the body are available in the test and the fixup.</span></span>

<span data-ttu-id="546fe-150">Für beide Schleifen Typen wird jeder Durchlauf der Schleife in einem eigenen Bereich ausgeführt, sodass Bindungen aus einem früheren Durchlauf in einem späteren Durchlauf nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="546fe-150">For both types of loops, each pass through the loop runs in its own scope, so bindings from an earlier pass are not available in a later pass.</span></span>
<span data-ttu-id="546fe-151">Weitere Informationen zu diesen Schleifen finden Sie unter [Ablauf Steuerung](xref:microsoft.quantum.guide.controlflow).</span><span class="sxs-lookup"><span data-stu-id="546fe-151">For more information on these loops, see [Control Flow](xref:microsoft.quantum.guide.controlflow).</span></span>

<span data-ttu-id="546fe-152">Innere Blöcke erben Symbol Bindungen von äußeren Blöcken.</span><span class="sxs-lookup"><span data-stu-id="546fe-152">Inner blocks inherit symbol bindings from outer blocks.</span></span>
<span data-ttu-id="546fe-153">Ein Symbol kann nur einmal pro Block gebunden werden. Es ist unzulässig, ein Symbol mit dem gleichen Namen wie ein anderes Symbol zu definieren, das sich im Gültigkeitsbereich befindet (kein "shadodown").</span><span class="sxs-lookup"><span data-stu-id="546fe-153">You can only bind a symbol once per block; it is illegal to define a symbol with the same name as another symbol that is within scope (no "shadowing").</span></span>
<span data-ttu-id="546fe-154">Die folgenden Sequenzen sind zulässig:</span><span class="sxs-lookup"><span data-stu-id="546fe-154">The following sequences are legal:</span></span>

```qsharp
if (a == b) {
    ...
    let n = 5;
    ...             // n is 5
}
let n = 8;
...                 // n is 8
```

<span data-ttu-id="546fe-155">und</span><span class="sxs-lookup"><span data-stu-id="546fe-155">and</span></span>

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

<span data-ttu-id="546fe-156">Dies wäre jedoch unzulässig:</span><span class="sxs-lookup"><span data-stu-id="546fe-156">But this would be illegal:</span></span>

```qsharp
let n = 5;
...                 // n is 5
let n = 8;          // Error!!
...
```

<span data-ttu-id="546fe-157">wie folgt:</span><span class="sxs-lookup"><span data-stu-id="546fe-157">as would:</span></span>

```qsharp
let n = 8;
if (a == b) {
    ...             // n is 8
    let n = 5;      // Error!
    ...
}
...
```

## <a name="next-steps"></a><span data-ttu-id="546fe-158">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="546fe-158">Next steps</span></span>

<span data-ttu-id="546fe-159">Erfahren Sie mehr über das [Arbeiten mit Qubits](xref:microsoft.quantum.guide.qubits) in Q# .</span><span class="sxs-lookup"><span data-stu-id="546fe-159">Learn about [Working With Qubits](xref:microsoft.quantum.guide.qubits) in Q#.</span></span>
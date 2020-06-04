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
# <a name="variables-in-q"></a>Variablen in Q #

Q # unterscheidet zwischen veränderbaren und unveränderlichen Symbolen oder "Variables", die an Ausdrücke gebunden/zugewiesen sind.
Im Allgemeinen wird die Verwendung unveränderlicher Symbole empfohlen, da es dem Compiler ermöglicht, weitere Optimierungen auszuführen.

Die linke Seite einer Bindung besteht aus einem symboltupel und der rechten Seite eines Ausdrucks.

## <a name="immutable-variables"></a>Unveränderliche Variablen

Ein Wert eines beliebigen Typs in Q # kann einer Variablen für die Wiederverwendung innerhalb eines Vorgangs oder einer Funktion mithilfe des `let` Schlüssel Worts zugewiesen werden.

Eine unveränderliche Bindung besteht aus dem Schlüsselwort `let` , gefolgt von einem Symbol oder einem symboltupel, einem Gleichheitszeichen `=` , einem Ausdruck, an den die Symbole gebunden werden, und einem abschließenden Semikolon.

Zum Beispiel:

```qsharp
let measurementOperator = [PauliX, PauliZ, PauliZ, PauliX, PauliI];
```

Dadurch wird dem Variablennamen (oder "Symbol") ein bestimmtes Array von Pauli-Operatoren zugewiesen `measurementOperator` .

> [!NOTE]
> Der Typ der neuen Variablen muss nicht explizit angegeben werden, da der Ausdruck auf der rechten Seite der `let` Anweisung eindeutig ist und der Typ vom Compiler abgeleitet wird. 

Mit definierte Variablen `let` sind *unveränderlich*, d. h., nachdem Sie definiert wurde, kann Sie nicht mehr geändert werden.
Dies ermöglicht eine Reihe nützlicher Optimierungen, einschließlich der Optimierung der klassischen Logik, die auf Variablen angewendet wird, die für die Anwendung der `Adjoint` Variante eines Vorgangs neu angeordnet werden.

## <a name="mutable-variables"></a>Änderbare Variablen

Als Alternative zum Erstellen einer Variablen mit `let` wird mit dem- `mutable` Schlüsselwort eine änderbare Variable erstellt, die nach der anfänglichen Erstellung mithilfe des Schlüssel Worts erneut gebunden werden *kann* `set` .

Symbole, die als Teil einer-Anweisung deklariert und gebunden `mutable` werden, können später im Code an einen anderen Wert zurückgebunden werden. Wenn ein Symbol später im Code wieder verwendet wird, wird der Typ nicht geändert, und der neu gebundene Wert muss mit diesem Typ kompatibel sein.

### <a name="rebinding-of-mutable-symbols"></a>Neubinden von änderbaren Symbolen

Eine änderbare Variable kann mit einer-Anweisung wieder verwendet werden `set` .
Eine solche erneute Bindung besteht aus dem Schlüsselwort `set` , gefolgt von einem Symbol oder einem symboltupel, einem Gleichheitszeichen `=` , einem Ausdruck zum erneuten Binden der Symbole an und einem abschließenden Semikolon.

Hier finden Sie einige Beispiele für Methoden zur Neubindung von Anweisungen.

### <a name="apply-and-reassign-statements"></a>Apply-and-REASSIGN-Anweisungen

Eine bestimmte Art von `set` -Anweisung, auf die als *Apply-and-REASSIGN* -Anweisung verwiesen wird, stellt eine bequeme Methode für die Verkettung dar, wenn die Rechte Seite aus der Anwendung eines binären Operators besteht und das Ergebnis an das linke Argument des Operators gebunden werden soll. Beispiel:
```qsharp
mutable counter = 0;
for (i in 1 .. 2 .. 10) {
    set counter += 1;
    // ...
}
```
Inkremente `counter` in jeder Iterations Schleife den Wert des Zählers `for` . Der obige Code entspricht 
```qsharp
mutable counter = 0;
for (i in 1 .. 2 .. 10) {
    set counter = counter + 1;
    // ...
}
```

Ähnliche Anweisungen sind für alle binären Operatoren verfügbar, in denen der Typ der linken Seite mit dem Ausdruckstyp übereinstimmt. Dies stellt beispielsweise eine bequeme Möglichkeit zum Sammeln von Werten dar.

Beispielsweise ist "supposiposiposiposiposiposiposiposiposierend" `qubits` ein regsiter
```qsharp
mutable results = new Result[0];   // results is an empty array of type Result[]
for (q in qubits) {
    set results += [M(q)];         // concatenate the outcome from measuring q to the existing array
    // ...
}
...                                // results contains the measurement outcomes from the whole register
```

### <a name="update-and-reassign-statements"></a>Update-und-REASSIGN-Anweisungen

Eine ähnliche Verkettung ist für [Kopier-und Update Ausdrücke](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions) auf der rechten Seite vorhanden.
Entsprechend sind *Update-und-REASSIGN* -Anweisungen für *benannte Elemente* in benutzerdefinierten Typen sowie für *Array Elemente*vorhanden.  

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

Im Fall von Arrays [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) stellt in unseren Standardbibliotheken die erforderlichen Tools für viele gängige Anforderungen an die Initialisierung und Bearbeitung von Arrays bereit, sodass es nicht erforderlich ist, Array Elemente an erster Stelle zu aktualisieren. 

Update-und-REASSIGN-Anweisungen stellen bei Bedarf eine Alternative dar:

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

Mithilfe der Bibliotheks Tools für Arrays, die in bereitgestellt werden, können Sie z. b. [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) einfach eine Funktion definieren, die ein Array von "Paulis" zurückgibt, bei dem der Pauli bei Index `i` den angegebenen Wert annimmt und alle anderen Einträge die Identität sind.

Im folgenden finden Sie zwei Definitionen einer solchen Funktion, wobei die zweite die von Ihnen zur Verfügung stehenden Tools nutzt.

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

Anstatt jeden Index im Array zu durchlaufen und ihn bedingt auf oder festzulegen `PauliI` `Pauli` , können wir stattdessen aus verwenden, `ConstantArray` [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) um ein Array von zu erstellen `PauliI` , und dann einfach einen Copy-and-Update-Ausdruck zurückgeben, in dem wir den bestimmter-Wert bei Index geändert haben `location` :

```qsharp
function PauliEmbedding(pauli : Pauli, length : Int, location : Int) : Pauli[] {
    return ConstantArray(length, PauliI) w/ location <- pauli;
}
```

## <a name="tuple-deconstruction"></a>Tupelerstellung

Zusätzlich zum Zuweisen einer einzelnen Variablen werden die `let` `mutable` Schlüsselwörter und---oder tatsächlich jedes andere Bindungs Konstrukt, wie z. b. `set` (unten beschrieben),---auch das Entpacken des Inhalts eines [tupeltyps](xref:microsoft.quantum.guide.types#tuple-types)ermöglichen.
Eine Zuweisung dieses Formulars heißt, dass die Elemente dieses Tupels *deaktiviert* werden.

Wenn die Rechte Seite der Bindung ein Tupel ist, kann dieses Tupel bei der Zuweisung dekonstruiert werden.
Solche Dekonstruktionen können geschaltete Tupel einschließen, und jede vollständige oder partielle Dekonstruktion ist gültig, solange die Form des Tupels auf der rechten Seite mit der Form des symboltupels kompatibel ist.

Beispiel:

```qsharp
let (i, f) = (5, 0.1); // i is bound to 5 and f to 0.1
mutable (a, (_, b)) = (1, (2, 3)); // a is bound to 1, b is bound to 3
mutable (x, y) = ((1, 2), [3, 4]); // x is bound to (1,2), y is bound to [3,4]
set (x, _, y) = ((5, 6), 7, [8]);  // x is rebound to (5,6), y is rebound to [8]
let (r1, r2) = MeasureTwice(q1, PauliX, q2, PauliY);
```

## <a name="binding-scopes"></a>Bindungs Bereiche

Im allgemeinen verlassen Symbol Bindungen den Gültigkeitsbereich und werden am Ende des Anweisungsblocks, in dem Sie auftreten, inaktiv.
Es gibt jedoch zwei Ausnahmen:

- Die Bindung der Schleifen Variablen einer Schleife liegt im Gültigkeitsbereich des Texts der `for` for-Schleife, aber nicht nach dem Ende der Schleife.
- Alle drei Teile einer `repeat` / `until` Schleife (der Text, der Test und das Fixup) werden als einzelner Bereich behandelt, sodass im Text gebundene Symbole im Test und im Fixup verfügbar sind.

Für beide Schleifen Typen wird jeder Durchlauf der Schleife in einem eigenen Bereich ausgeführt, sodass Bindungen aus einem früheren Durchlauf in einem späteren Durchlauf nicht verfügbar sind.
Details zu diesen Schleifen finden Sie unter [Ablauf Steuerung](xref:microsoft.quantum.guide.controlflow).

Symbol Bindungen aus äußeren Blöcken werden von inneren Blöcken geerbt.
Ein Symbol kann nur einmal pro Block gebunden werden. Es ist unzulässig, ein Symbol mit dem gleichen Namen wie ein anderes Symbol zu definieren, das sich im Gültigkeitsbereich befindet (kein "shadodown").
Die folgenden Sequenzen sind zulässig:

```qsharp
if (a == b) {
    ...
    let n = 5;
    ...             // n is 5
}
let n = 8;
...                 // n is 8
```

and

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

Dies wäre jedoch unzulässig:

```qsharp
let n = 5;
...                 // n is 5
let n = 8;          // Error!!
...
```

wie folgt:

```qsharp
let n = 8;
if (a == b) {
    ...             // n is 8
    let n = 5;      // Error!
    ...
}
...
```

## <a name="next-steps"></a>Nächste Schritte

Erfahren Sie mehr über das [Arbeiten mit Qubits](xref:microsoft.quantum.guide.qubits) in f #.
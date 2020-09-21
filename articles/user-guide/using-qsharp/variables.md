---
title: Variablen in Q#
description: Erfahren Sie, wie Sie mit verschiedenen Variablen in arbeiten können. Q#
author: gillenhaalb
ms.author: a-gibec
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.variables
no-loc:
- Q#
- $$v
ms.openlocfilehash: bb87f36d3c9b7df195f64e85151e833d494ea945
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/21/2020
ms.locfileid: "90835875"
---
# <a name="variables-in-no-locq"></a>Variablen in Q#

Q# unterscheidet zwischen veränderbaren und unveränderlichen Symbolen oder *Variablen*, die an Ausdrücke gebunden/zugewiesen sind.
Im Allgemeinen wird die Verwendung unveränderlicher Symbole empfohlen, da es dem Compiler ermöglicht, weitere Optimierungen auszuführen.

Die linke Seite einer Bindung besteht aus einem symboltupel und der rechten Seite eines Ausdrucks.

## <a name="immutable-variables"></a>Unveränderliche Variablen

Sie können einen Wert eines beliebigen Typs in Q# einer Variablen für die Wiederverwendung innerhalb eines Vorgangs oder einer Funktion mithilfe des `let` Schlüssel Worts zuweisen. 

Eine unveränderliche Bindung besteht aus dem Schlüsselwort `let` , gefolgt von einem Symbol oder einem symboltupel, einem Gleichheitszeichen `=` , einem Ausdruck, an den die Symbole gebunden werden, und einem abschließenden Semikolon.

Beispiel:

```qsharp
let measurementOperator = [PauliX, PauliZ, PauliZ, PauliX, PauliI];
```

Dadurch wird dem Variablennamen (oder "Symbol") ein bestimmtes Array von Pauli-Operatoren zugewiesen `measurementOperator` .

> [!NOTE]
> Im vorherigen Beispiel muss der Typ der neuen Variablen nicht explizit angegeben werden, da der Ausdruck auf der rechten Seite der `let` Anweisung eindeutig ist, und der Compiler leitet den richtigen Typ ab. 

Variablen `let` , die mit definiert werden, sind *unveränderlich*. Dies bedeutet, dass Sie nach der Definition nicht mehr in irgendeiner Weise geändert werden können.
Dies ermöglicht eine Reihe nützlicher Optimierungen, einschließlich der Optimierung der klassischen Logik, die für die Neuanordnung von Variablen zum Anwenden der `Adjoint` Variante eines Vorgangs durchgesetzt wird.

## <a name="mutable-variables"></a>Änderbare Variablen

Als Alternative zum Erstellen einer Variablen mit `let` erstellt das- `mutable` Schlüsselwort eine änderbare Variable, die nach der anfänglichen Erstellung mithilfe des-Schlüssel Worts wieder hergestellt werden *kann* `set` .

Sie können Symbole, die als Teil einer Anweisung deklariert und als Teil einer Anweisung gebunden wurden `mutable` , an einen anderen Wert weiter unten im Code binden. Wenn ein Symbol später im Code wieder verwendet wird, wird der Typ nicht geändert, und der neu gebundene Wert muss mit diesem Typ kompatibel sein.

### <a name="rebinding-of-mutable-symbols"></a>Neubinden von änderbaren Symbolen

Sie können eine änderbare Variable mithilfe einer-Anweisung erneut binden `set` .
Eine solche erneute Bindung besteht aus dem Schlüsselwort `set` , gefolgt von einem Symbol oder einem symboltupel, einem Gleichheitszeichen `=` , einem Ausdruck zum erneuten Binden der Symbole an und einem abschließenden Semikolon.

Im folgenden finden Sie einige Beispiele für Methoden zur Neubindung von Anweisungen.

#### <a name="apply-and-reassign-statements"></a>Apply-and-REASSIGN-Anweisungen

Eine bestimmte Art von `set` -Anweisung, die *Apply-and-REASSIGN* -Anweisung, stellt eine bequeme Möglichkeit zur Verkettung dar, wenn die Rechte Seite aus der Anwendung eines binären Operators besteht und das Ergebnis an das linke Argument des Operators zurückgesetzt werden soll. Beispiel:

```qsharp
mutable counter = 0;
for (i in 1 .. 2 .. 10) {
    set counter += 1;
    // ...
}
```
Inkremente `counter` in jeder Iterations Schleife den Wert des Zählers `for` . Der vorherige Code entspricht. 

```qsharp
mutable counter = 0;
for (i in 1 .. 2 .. 10) {
    set counter = counter + 1;
    // ...
}
```

Ähnliche Anweisungen sind für alle binären Operatoren verfügbar, in denen der Typ der linken Seite mit dem Ausdruckstyp übereinstimmt. Diese Anweisungen stellen eine bequeme Möglichkeit zum Sammeln von Werten dar.

Beispielsweise ist die Untersetzung `qubits` ein Register von Qubits:
```qsharp
mutable results = new Result[0];   // results is an empty array of type Result[]
for (q in qubits) {
    set results += [M(q)];         // concatenate the outcome from measuring q to the existing array
    // ...
}
...                                // results contains the measurement outcomes from the whole register
```

#### <a name="update-and-reassign-statements"></a>Update-und-REASSIGN-Anweisungen

Eine ähnliche Verkettung ist für [Copy-und Update-Ausdrücke](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions) auf der rechten Seite vorhanden.
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

Im Fall von Arrays [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) stellt in der Q# Standardbibliothek die erforderlichen Tools für viele gängige Anforderungen an die Initialisierung und Bearbeitung von Arrays bereit, sodass es nicht erforderlich ist, Array Elemente an erster Stelle zu aktualisieren. 

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

Mithilfe der Bibliotheks Tools für Arrays, die in bereitgestellt werden, [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) können Sie z. b. problemlos eine Funktion definieren, die ein Array von Typen zurückgibt, `Pauli` wobei das Element bei Index `i` einen bestimmten `Pauli` Wert annimmt und alle anderen Einträge die Identität ( `PauliI` ) sind.

Im folgenden finden Sie zwei Definitionen einer solchen Funktion, wobei die zweite die von Ihnen zur Verfügung stehenden Tools nutzt.

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

Anstatt jeden Index im Array zu durchlaufen und ihn bedingt auf `PauliI` oder das angegebene festzulegen `pauli` , können Sie stattdessen in verwenden, `ConstantArray` [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) um ein Array von Typen zu erstellen `PauliI` , und dann einfach einen Copy-and-Update-Ausdruck zurückgeben, in dem Sie den spezifischen Wert bei Index geändert haben `location` :

```qsharp
function PauliEmbedding(pauli : Pauli, length : Int, location : Int) : Pauli[] {
    return ConstantArray(length, PauliI) w/ location <- pauli;
}
```

## <a name="tuple-deconstruction"></a>Tupelerstellung

Zusätzlich zum Zuweisen einer einzelnen Variablen können Sie die `let` `mutable` Schlüsselwörter und oder ein beliebiges anderes Bindungs Konstrukt verwenden, z `set` . b., um den Inhalt eines [tupeltyps](xref:microsoft.quantum.guide.types#tuple-types)zu entpacken.
Eine Zuweisung dieses Formulars heißt, dass die Elemente dieses Tupels *deaktiviert* werden.

Wenn die Rechte Seite der Bindung ein Tupel ist, können Sie dieses Tupel bei der Zuweisung dekonstruieren.
Solche Dekonstruktionen können geschaltete Tupel einschließen, und jede vollständige oder partielle Dekonstruktion ist gültig, solange die Form des Tupels auf der rechten Seite mit der Form des symboltupels kompatibel ist.

Zum Beispiel:

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
- Alle drei Teile einer `repeat` / `until` Schleife (der Text, der Test und das Fixup) fungieren als einzelner Bereich, sodass im Text gebundene Symbole im Test und im Fixup verfügbar sind.

Für beide Schleifen Typen wird jeder Durchlauf der Schleife in einem eigenen Bereich ausgeführt, sodass Bindungen aus einem früheren Durchlauf in einem späteren Durchlauf nicht verfügbar sind.
Weitere Informationen zu diesen Schleifen finden Sie unter [Ablauf Steuerung](xref:microsoft.quantum.guide.controlflow).

Innere Blöcke erben Symbol Bindungen von äußeren Blöcken.
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

und

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

Erfahren Sie mehr über das [Arbeiten mit Qubits](xref:microsoft.quantum.guide.qubits) in Q# .
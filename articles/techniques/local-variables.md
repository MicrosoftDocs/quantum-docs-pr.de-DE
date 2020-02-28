---
title: 'Lokale Variablen-Q #-Techniken'
description: 'Erfahren Sie, wie Sie lokale Variablen in Q # definieren und mit Ihnen arbeiten.'
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.techniques.local-variables
ms.openlocfilehash: cb6c662137c31a13c3dd6e9ca3f67879c469f788
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2020
ms.locfileid: "77906864"
---
# <a name="local-variables"></a>Lokale Variablen #

Ein Wert eines beliebigen Typs in Q # kann einer Variablen für die Wiederverwendung innerhalb eines Vorgangs oder einer Funktion mithilfe des `let`-Schlüssel Worts zugewiesen werden.
Beispiel:

```qsharp
let measurementOperator = [PauliX, PauliZ, PauliZ, PauliX, PauliI];
```

Dadurch wird einer Variablen mit dem Namen `measurementOperator`ein bestimmtes Array von Pauli-Operatoren zugewiesen.

> [!TIP]
> Beachten Sie, dass der Typ der neuen Variablen nicht explizit angegeben werden muss, da der Ausdruck auf der rechten Seite der `let` Anweisung eindeutig ist und der Typ vom Compiler abgeleitet wird. 

Variablen in Q # sind *unveränderlich*. Dies bedeutet, dass eine Variable nicht mehr geändert werden kann, sobald eine Variable auf diese Weise definiert wurde.
Dies ermöglicht eine Reihe nützlicher Optimierungen, einschließlich der Optimierung der klassischen Logik, die auf Variablen angewendet wird, die für die Anwendung der `Adjoint` Variant eines Vorgangs neu angeordnet werden.

Variablen, die mit der `let` Bindung wie oben definiert definiert sind, sind für einen bestimmten Bereich lokal, z. b. den Text eines Vorgangs oder den Inhalt einer `for` Schleife.


## <a name="mutability"></a>Veränderlichkeit ##

Als Alternative zum Erstellen einer Variablen mit `let`erstellt das `mutable`-Schlüsselwort eine spezielle änderbare Variable, die nach der anfänglichen Erstellung mithilfe des `set`-Schlüssel Worts erneut gebunden werden kann.

```qsharp
operation RandomInts(maxInt : Int, nrSamples : Int) : Int[] {
    mutable samples = new Int[0];
    for (i in 1 .. nrSamples) {
        set samples += [RandomInt(maxInt)];
    }
    return samples;
}
```

Alle Typen in Q #, einschließlich Arrays, folgen der Wert Semantik. Insbesondere ist es nicht möglich, Array Elemente zu aktualisieren. Wenn Sie ein vorhandenes Array ändern möchten, müssen Sie einen Kopier-und Aktualisierungsmechanismus ähnlich dem für F#Datensätze in nutzen. Mithilfe der Bibliotheks Tools für Arrays, die in [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays)bereitgestellt werden, können wir einfach eine Funktion definieren, die ein Array von Paulis zurückgibt, bei dem der Pauli bei Index `i` den angegebenen Wert annimmt und alle anderen Einträge die Identität sind: 

```qsharp
function EmbedPauli (pauli : Pauli, i : Int, n : Int) : Pauli[] {
    
    let arr = ConstantArray(n, PauliI); // creates an array of filled with PauliI
    return arr w/ i <- pauli; // constructs a new array based on arr except that entry i is set to pauli
}
```

Weitere Informationen zum Arbeiten mit Arrays finden Sie bei der Erörterung von Q #-Anweisungen und-Ausdrücken. 

Die muability in Q # ist ein Konzept, das für ein *Symbol* anstelle eines Typs oder Werts gilt. Insbesondere weist Sie weder implizit noch explizit eine Darstellung im Typsystem auf, und ob eine Bindung änderbar (wie durch das `mutable`-Schlüsselwort angegeben) oder unveränderlich (wie durch `let`angegeben) nicht den Typ der gebundenen Variablen ändert. Dies bietet eine wichtige Möglichkeit zum Isolieren der muability in spezialisierten Funktionen und Vorgängen.
Insbesondere, obwohl eine Adjoint-Spezialisierung für einen Vorgang, der eine änderbare Variable verwendet, nicht automatisch generiert werden kann, funktioniert die automatische Generierung problemlos für einen Vorgang, der eine Funktion aufrufen, die Veränderlichkeit verwendet.
Aus diesem Grund empfiehlt es sich, Funktionen und Vorgänge zu erstellen, die die Änderbarkeit so kurz und kompakt wie möglich verwenden, sodass der Rest des Quantum-Programms mithilfe normaler unveränderlicher Variablen geschrieben werden kann.


## <a name="deconstruction"></a>Dekonstruktion ##

Zusätzlich zum Zuweisen einer einzelnen Variablen ermöglichen die `let`-und `mutable` Schlüsselwörter bzw. ein beliebiges anderes Bindungs Konstrukt auch das Entpacken des Inhalts eines [tupeltyps](xref:microsoft.quantum.language.type-model#tuple-types).
Eine Zuweisung dieses Formulars heißt, dass die Elemente dieses Tupels *deaktiviert* werden.
Wenn wir beispielsweise einen Begriff in einer hamiltona durch ein Tupel modellieren, können wir die Debug-Methode verwenden, um auf die verschiedenen Daten zuzugreifen, die wir unter diesem Begriff simulieren müssen:

```qsharp
// Represents H = 3.1 X_0 Z_1.
let (_, (paulis, idxQubits)) = ((3.1, 1.0), ([PauliX, PauliZ], [0, 1])); // paulis and idxQubits are both immutable variables
mutable ((c1, c2), _) = ((3.1, 1.0), ([PauliX, PauliZ], [0, 1])); // c1 and c2 are both mutable variables
```



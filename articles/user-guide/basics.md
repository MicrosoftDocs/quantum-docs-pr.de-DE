---
title: 'F #-Grundlagen'
description: 'Grundlegende Konzepte von Q #'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 02/28/2020
ms.topic: article
uid: microsoft.quantum.guide.basics
ms.openlocfilehash: fd0ea47f00b1456ec460808ef7d451c8427677cd
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2020
ms.locfileid: "83431154"
---
# <a name="q-basics"></a>F #-Grundlagen

In diesem Abschnitt wird eine kurze Einführung in die grundlegenden Bausteine von Q # vorgestellt.

Eine kurze Übersicht darüber, was q # ist und wo es als grundlegende Komponente des Quantum Development Kit passt, finden Sie unter [Was ist q #?](xref:microsoft.quantum.overview.q-sharp). 

## <a name="what-is-a-quantum-program"></a>Was ist ein Quantum-Programm?

Aus technischer Sicht kann ein Quantum-Programm als ein bestimmter Satz klassischer Unterroutinen angesehen werden, die beim Aufruf bestimmte Vorgänge auf einem Quantum-System ausführen.
Eine wichtige Konsequenz dieser Ansicht besteht darin, dass ein in Q # geschriebenes Programm Qubits selbst nicht direkt modelliert, sondern vielmehr beschreibt, wie ein klassischer Steuerungscomputer mit diesen Qubits interagiert.
Entwurfs bedingt definiert f # daher nicht die Quantum-Zustände oder andere Eigenschaften von Quantum-Mechanismen direkt.
Sehen Sie sich beispielsweise den Status $ \ket{+} = \left (\ket {0} + \ket {1} \right)/\sqrt {2} $ an, der im Handbuch für die [Quantum Computing-Konzepte](xref:microsoft.quantum.concepts.intro) erläutert wird.
Um diesen Status in Q # vorzubereiten, verwenden wir die Fakten, die die Qubits im Zustand "$ \ket $" initialisiert werden {0} , und "$ \ket{+} = h\ket {0} $", wobei "$H $" die durch [ `H` Operation] (] (Xref: Microsoft. Quantum. intrinsid. H) implementierte Hadamard-Transformation ist:

```qsharp
using (qubit = Qubit()) {
    // At this point, qubit is in the state |0⟩.
    H(qubit);
    // We've now applied H, such that our qubit is in H|0⟩ = |+⟩, as we wanted.
}
```

## <a name="quantum-states-in-q"></a>Quantum-Zustände in Q #

Wichtig: beim Schreiben des obigen Programms haben wir nicht explizit auf den Bundesstaat in Q # verwiesen, sondern vielmehr beschrieben, wie der Zustand von unserem Programm *transformiert* wurde.
Dies ermöglicht es uns, unabhängig davon, was ein Quantum-Status *ist* , auch auf jedem Zielcomputer zu sein, der je nach Computer unterschiedliche Interpretationen aufweisen kann. 

Ein Q #-Programm hat keine Möglichkeit, den Zustand eines Qubit zu überprüfen.
Stattdessen kann ein Programm Vorgänge wie z. b. [`Measure`](xref:microsoft.quantum.intrinsic.measure) zum Erlernen von Informationen aus einem Qubit und zum Abrufen von Vorgängen wie [`X`](xref:microsoft.quantum.intrinsic.x) und [`H`](xref:microsoft.quantum.intrinsic.h) zum reagieren auf den Zustand eines Qubits aufzurufen.
Diese Vorgänge *werden tatsächlich nur* vom Zielcomputer durchgeführt, mit dem das jeweilige Q #-Programm ausgeführt wird.
Wenn Sie das Programm z. b. in unserem [vollständigen Simulator](xref:microsoft.quantum.machines.full-state-simulator)ausführen, führt der Simulator die entsprechenden mathematischen Operationen für das simulierte Quantum-System aus.
Wenn der Zielcomputer jedoch ein echter Quantum-Computer ist, wird der Quantum-Computer durch das aufrufen solcher Vorgänge in Q # an die Zukunft weitergeleitet, um die entsprechenden *echten* Vorgänge auf dem *realen* Quantum-System auszuführen (z. b. genau zeitgesteuerte Laserpulse).

Ein Q #-Programm kombiniert diese Vorgänge neu, wie von einem Zielcomputer definiert, um neue Vorgänge auf höherer Ebene zu erstellen, um die Quantum-Berechnung auszudrücken.
Auf diese Weise vereinfacht f # das Ausdrücken der Logik zugrunde liegenden Quantum-und Hybrid-Quantum – klassische Algorithmen und ist gleichzeitig in Bezug auf die Struktur eines Ziel Computers oder Simulators allgemein.

## <a name="q-operations-and-functions"></a>F #-Vorgänge und-Funktionen

Konkret besteht ein Q #-Programm aus *Vorgängen*, *Funktionen*und benutzerdefinierten Typen. 

Vorgänge werden verwendet, um die Transformationen von Quantum-Systemen zu beschreiben, und sind die grundlegendsten Bausteine von Q #-Programmen. Jeder in Q # definierte Vorgang kann dann eine beliebige Anzahl anderer Vorgänge aufzurufen.

Im Gegensatz zu Vorgängen werden Funktionen verwendet, um reines *deterministisches* klassisches Verhalten zu beschreiben, und Sie haben keine Auswirkungen, außer wenn Sie klassische Werte berechnen. Angenommen, wir möchten unsere Qubits am Ende eines Programms messen und die Messergebnisse einem Array hinzufügen.
In diesem Fall `Measure` ist ein *Vorgang* , der den Zielcomputer anweist, eine Messung der (realen oder simulierten) Qubits durchzuführen, und der klassische Prozess des Hinzufügens der zurückgegebenen Ergebnisse zu einem Array wird von *Functions*behandelt.

Vorgänge und Funktionen werden als *callables*bezeichnet, und die zugrunde liegende Struktur und das zugehörige Verhalten werden auf der Seite " [Vorgänge und Funktionen" in der f #](xref:microsoft.quantum.guide.operationsfunctions) -Seite eingeführt.


## <a name="q-syntax-overview"></a>Übersicht über die Q #-Syntax

Die Syntax einer Sprache beschreibt die verschiedenen Kombinationen von Symbolen, die ein syntaktisch korrektes Programm bilden.
In Q # können wir die Elemente der Syntax in drei verschiedenen Gruppen klassifizieren: Typen, Ausdrücke und Anweisungen.

### <a name="types"></a>Typen
F # ist eine stark typisierte Sprache, sodass der Compiler durch die sorgfältige Verwendung von Typen bei der Kompilierung starke Garantien für Q #-Programme bereitstellen kann.
Zusätzlich zu den standardmäßigen und Quantum-spezifischen, integrierten primitiven Typen (z. b.,, `Int` `Bool` `Qubit` und `Result` ) bietet Q # Unterstützung für benutzerdefinierte Typen.
Alle verschiedenen primitiven Typen von q # werden auf der Seite [Typen in q #](xref:microsoft.quantum.guide.types) sowie Details zu Array-und Tupeltypen beschrieben. Außerdem wird erläutert, wie Sie neue Typen in einer q #-Datei definieren.

### <a name="expressions"></a>Ausdrücke
Ein Ausdruck in einer Programmiersprache ist eine Kombination aus einer oder mehreren Konstanten, Variablen, Operatoren und Funktionen, die von der Programmiersprache interpretiert und zu einem bestimmten Wert ausgewertet werden.
In den meisten Fällen können Ausdrücke dieses Typs für jeden Typ in einer Sprache entweder *Literale* oder Symbole sein, die an einen Wert dieses Typs gebunden sind.
Beispielsweise `5` ist ein `Int` Literalzeichen (also auch ein Ausdruck vom Typ `Int` ), und wenn das Symbol `count` an den ganzzahligen Wert gebunden ist `5` , dann `count` ist auch ein ganzzahliger Ausdruck.

Außerdem kann ein Ausdruck aus anderen Ausdrücken bestehen, die mit bestimmten Operatoren kombiniert werden.
Ein weiteres Beispiel für einen `Int` Ausdruck, der ergibt, `5` ist `2+3` .

Die möglichen Ausdrücke von Typen in q # sowie die kompatiblen Operatoren, die verwendet werden können, werden auf den [Typausdrücken in der f #](xref:microsoft.quantum.guide.expressions) -Seite ausführlich erläutert. 

### <a name="statements"></a>Anweisungen 
Eine-Anweisung ist eine syntaktische Einheit einer imperativen Programmiersprache, die eine auszuführende Aktion ausdrückt. -Anweisungen vergleichen mit Ausdrücken in, dass-Anweisungen keine Ergebnisse zurückgeben und ausschließlich für Ihre Nebeneffekte ausgeführt werden, während Ausdrücke immer ein Ergebnis zurückgeben und oft keine Nebeneffekte haben.
Dieser Unterschied wird häufig in einem Wortlaut beobachtet: ein Ausdruck wird ausgewertet, während eine-Anweisung ausgeführt wird.

Ein sehr einfaches Beispiel für eine-Anweisung in Q # ist das Zuweisen eines Symbols zu einem Ausdruck:
```qsharp
let count = 5;
```

Ein etwas interessanteres Beispiel ist die `for` -Anweisung, die Iterationen unterstützt und einen- *Anweisungsblock*enthält.
Angenommen `qubits` ist das Symbol, das an ein Register von Qubits gebunden ist (technisch gesehen vom Typ `Qubit[]` , d. h. ein Array von `Qubit` Typen). Then
```qsharp
for (qubit in qubits) {
    H(qubit);
}
```
ist eine-Anweisung, die jedes Qubit im Register durchläuft, wobei jeweils der-Vorgang ausgeführt wird `H` . Beachten Sie, dass `H(qubit);` auch eine-Anweisung in sich selbst ist.

Tatsächlich können alle Aufruf Ausdrücke vom Typ (die Aufruf baren Objekte `Unit` , die keine Informationen zurückgeben) als Anweisung verwendet werden.
Dies wird hauptsächlich beim Aufrufen von Vorgängen für Qubits verwendet, die zurückgeben, da der Zweck der- `Unit` Anweisung darin besteht, den impliziten Quantum-Zustand zu ändern.
Ausdrucks Auswertungs Anweisungen erfordern ein abschließendes Semikolon.

Fast jeder Aspekt eines Q #-Programms wird mithilfe von-Anweisungen erstellt, sodass keine einzelne Seite alle Informationen im Zusammenhang mit diesen Informationen umfassen kann.
Die lexikalische Struktur und die Formatierung werden jedoch auf der Seite " [f #-Dateistruktur](xref:microsoft.quantum.guide.filestructure) ", der Symbol Bindungs Zuweisung und dem Bereich unter [Variablen in q #](xref:microsoft.quantum.guide.variables)und Ablauf Steuerungs Schleifen, wie z `for` . b. der [Ablauf Steuerung in q #](xref:microsoft.quantum.guide.controlflow), beschrieben.


## <a name="whats-next"></a>Ausblick
Im weiteren Verlauf dieses Handbuchs erfahren Sie, wie Sie mit Q # komplexe Quantum-Programme über die grundlegenden Bausteine von Vorgängen, Funktionen und Typen erstellen.

Um zu beginnen, können Sie mit dem Kennenlernen von [Typen in f #](xref:microsoft.quantum.guide.types)beginnen.

Wenn Sie mehr über die Grundlagen und die Motivation hinter q # erfahren möchten, finden Sie weitere Informationen unter [Warum benötigen wir q #?](https://devblogs.microsoft.com/qsharp/why-do-we-need-q/).

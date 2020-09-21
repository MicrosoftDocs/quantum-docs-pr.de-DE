---
title: Q# Kenntnisse
description: Grundlegende Konzepte von Q#
author: gillenhaalb
ms.author: a-gibec
ms.date: 02/28/2020
ms.topic: article
uid: microsoft.quantum.guide.basics
no-loc:
- Q#
- $$v
ms.openlocfilehash: 86f6538cf383f4e7c14255b38cfb1c141c8f991b
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/21/2020
ms.locfileid: "90835518"
---
# <a name="no-locq-basics"></a>Q# Kenntnisse

Dieser Artikel bietet eine kurze Einführung in die grundlegenden Bausteine von Q# .

Einen Überblick darüber, was Q# und wo es als grundlegende Komponente des Quantum Development Kit passt, finden Sie unter [Was ist Q# ?](xref:microsoft.quantum.overview.q-sharp). 

## <a name="what-is-a-quantum-program"></a>Was ist ein Quantum-Programm?

Aus technischer Sicht handelt es sich bei einem Quantum-Programm um einen bestimmten Satz klassischer Unterroutinen, die, wenn Sie aufgerufen werden, bestimmte Vorgänge auf einem Quantum-System ausführen.
Eine wichtige Konsequenz dieser Ansicht besteht darin, dass ein Q# Programm Qubits nicht direkt modelliert, sondern vielmehr beschreibt, wie ein klassisch kontrollierter Computer mit diesen Qubits interagiert.
Entwurfs bedingt Q# definiert keine Quantenzustände oder anderen Eigenschaften von Quantum-Mechanismen direkt.
Sehen Sie sich beispielsweise den Status $ \ket{+} = \left (\ket {0} + \ket {1} \right)/\sqrt {2} $ an, der im Handbuch für die [Quantum Computing-Konzepte](xref:microsoft.quantum.concepts.intro) erläutert wird.
Wenn Sie diesen Status in vorbereiten möchten Q# , beginnen Sie mit den Fakten, die die Qubits im Zustand "$ \ket $" initialisiert werden {0} , und "$ \ket{+} = h\ket {0} $", wobei $H $ die vom [ `H` Vorgang](xref:microsoft.quantum.intrinsic.h)implementierte [Hadamard-Transformation](xref:microsoft.quantum.glossary#hadamard)ist. Der grundlegende Q# Code zum Initialisieren und Transformieren eines Qubit sieht dann wie folgt aus:

```qsharp
using (qubit = Qubit()) {
    // At this point, the qubit is in the state |0⟩.
    H(qubit);
    // H is now applied, such that the qubit is in H|0⟩ = |+⟩, as desired.
}
```
Weitere Informationen zum Initialisieren oder *zuordnen*von Qubits finden Sie unter [Arbeiten mit Qubits](xref:microsoft.quantum.guide.qubits).

## <a name="quantum-states-in-no-locq"></a>Quantum-Zustände in Q#

Wichtig ist, dass das vorherige Programm nicht explizit auf den Bundesstaat verweist, Q# sondern beschreibt, wie das Programm den Zustand *transformiert* hat.
Bei dieser Vorgehensweise können Sie unabhängig davon, was ein Quantum-Status *ist* , auf jedem Zielcomputer, der je nach Computer unterschiedliche Interpretationen aufweisen kann, vollständig agnostisch sein. 

Ein Q# Programm kann nicht in den Zustand eines Qubit-Felds hinein geraten.
Stattdessen kann ein Programm Vorgänge wie z. b. [`Measure`](xref:microsoft.quantum.intrinsic.measure) zum Erlernen von Informationen aus einem Qubit und zum Aufzählen von Vorgängen, z. b. und, verwenden, [`X`](xref:microsoft.quantum.intrinsic.x) [`H`](xref:microsoft.quantum.intrinsic.h) um auf den Zustand eines Qubit zu reagieren.
Diese Vorgänge *werden tatsächlich nur* vom Zielcomputer durchgeführt, der zum Ausführen des jeweiligen Programms verwendet wurde Q# .
Wenn Sie das Programm z. b. in unserem [vollständigen Simulator](xref:microsoft.quantum.machines.full-state-simulator)ausführen, führt der Simulator die entsprechenden mathematischen Operationen für das simulierte Quantum-System aus.
Wenn der Zielcomputer jedoch ein echter Quantum-Computer ist, wird der Quantum-Computer durch den Aufruf solcher Vorgänge in angewiesen, Q# die entsprechenden *echten* Vorgänge auf dem *realen* Quantum-System auszuführen, z. b. genau zeitgesteuerte Laserpulse.

Ein Q# Programm kombiniert diese Vorgänge so, wie Sie von einem Zielcomputer definiert wurden, um neue Vorgänge auf höherer Ebene zum Ausdrücken von Quantum-Berechnungen zu erstellen.
Auf diese Weise ist Q# es einfacher, die Logik zugrunde liegende Quantum und Hybrid Quantum – klassische Algorithmen auszudrücken, während dies auch in Bezug auf die Struktur eines Ziel Computers oder Simulators allgemein ist.

## <a name="no-locq-operations-and-functions"></a>Q# Vorgänge und Funktionen

Konkret umfasst ein Q# Programm *Vorgänge*, *Funktionen*und beliebige benutzerdefinierte Typen. 

Vorgänge werden verwendet, um die Transformationen von Quantum-Systemen zu beschreiben, und sind die grundlegendsten Bausteine von Q# Programmen. Jeder in definierte Vorgang Q# kann dann eine beliebige Anzahl anderer Vorgänge aufzurufen.

Im Gegensatz zu Vorgängen werden Funktionen verwendet, um reines *deterministisches* klassisches Verhalten zu beschreiben, und Sie haben keine Auswirkungen, außer wenn Sie klassische Werte berechnen. Angenommen, Sie möchten die Qubits am Ende eines Programms messen und die Messergebnisse einem Array hinzufügen.
In diesem Fall `Measure` ist ein *Vorgang* , der den Zielcomputer anweist, eine Maßeinheit für die (echte oder simulierte) Qubits auszuführen. Gleichzeitig verarbeiten *Funktionen* den klassischen Prozess des Hinzufügens der zurückgegebenen Ergebnisse zu einem Array.

Vorgänge und Funktionen werden auch als *callables*bezeichnet. Die zugrunde liegende Struktur und das zugehörige Verhalten werden in [Vorgängen und Q# Funktionen in ](xref:microsoft.quantum.guide.operationsfunctions)eingeführt und ausführlich erläutert.


## <a name="no-locq-syntax-overview"></a>Q# Syntax Übersicht

Die Syntax einer Sprache beschreibt die verschiedenen Kombinationen von Symbolen, die ein syntaktisch korrektes Programm bilden.
In Q# werden Syntax Elemente in drei unterschiedliche Gruppen eingeteilt: Typen, Ausdrücke und Anweisungen.

### <a name="types"></a>Typen
Q# ist eine stark typisierte Sprache, sodass der Compiler bei der sorgfältigen Verwendung von Typen bei der Kompilierung starke Garantien für Programme bereitstellen kann Q# .
Zusätzlich zu den standardmäßigen und Quantum-spezifischen integrierten primitiven Typen, z. b. `Int` , `Bool` , `Qubit` und `Result` , Q# bietet Unterstützung für benutzerdefinierte Typen.

Beschreibungen aller primitiven Typen, Details zu Array-und Tupeltypen sowie Schritte zum Definieren neuer Typen innerhalb einer Q# Datei finden Sie unter [Typen in Q# ](xref:microsoft.quantum.guide.types).

### <a name="expressions"></a>Ausdrücke
Ein Ausdruck in einer Programmiersprache ist eine Kombination aus einer oder mehreren Konstanten, Variablen, Operatoren und Funktionen, die von der Programmiersprache interpretiert und zu einem bestimmten Wert ausgewertet werden.
In den meisten Fällen können Ausdrücke dieses Typs für jeden Typ in einer Sprache entweder *Literale* oder Symbole sein, die an einen Wert dieses Typs gebunden sind.
Beispielsweise `5` ist ein `Int` Literalzeichen (also auch ein Ausdruck vom Typ `Int` ), und wenn das Symbol `count` an den ganzzahligen Wert gebunden ist `5` , dann `count` ist auch ein ganzzahliger Ausdruck.

Außerdem kann ein Ausdruck aus anderen Ausdrücken bestehen, die von bestimmten Operatoren kombiniert werden.
Ein anderer Ausdruck, `Int` der ergibt, ist z `5` . b `2+3` ..

Weitere Informationen zu Ausdrücken und kompatiblen Operatoren in Q# finden Sie unter [typausdrücke Q# in ](xref:microsoft.quantum.guide.expressions). 

### <a name="statements"></a>Anweisungen 
Eine-Anweisung ist eine syntaktische Einheit einer imperativen Programmiersprache, die einige auszuführende Aktionen ausdrückt. Anweisungen, die mit Ausdrücken in der Anweisung vergleichen, geben keine Ergebnisse zurück und werden ausschließlich für Ihre Nebeneffekte ausgeführt. Ausdrücke geben jedoch immer ein Ergebnis zurück und haben oft keine Nebeneffekte. Kurz gesagt Q# werden-Anweisungen ausgeführt, während Ausdrücke ausgewertet werden.

Ein einfaches Beispiel für eine-Anweisung in Q# ist das Zuweisen eines Symbols zu einem Ausdruck:
```qsharp
let count = 5;
```

Ein interessanteres Beispiel ist die `for` -Anweisung, die Iterationen unterstützt und einen- *Anweisungsblock*enthält.
Angenommen `qubits` ist das Symbol, das an ein Register von Qubits gebunden ist (technisch gesehen vom Typ `Qubit[]` oder ein Array von `Qubit` Typen). Then
```qsharp
for (qubit in qubits) {
    H(qubit);
}
```
ist eine-Anweisung, die jedes Qubit im Register durchläuft, wobei jeweils der Vorgang durchgeführt wird `H` . Beachten Sie, dass `H(qubit);` auch eine-Anweisung in sich selbst ist.

Sie können einen beliebigen aufrufsausdruck vom Typ `Unit` (ein `Unit` Typ gibt keine Informationen zurückgeben) als-Anweisung verwenden.
Diese Art von Ausdruck ist nützlich, wenn Vorgänge für Qubits aufgerufen werden, die zurückgeben, `Unit` da der Zweck der Anweisung darin besteht, den impliziten Quantum-Zustand zu ändern.
Ausdrucks Auswertungs Anweisungen erfordern ein abschließendes Semikolon.

Sie verwenden-Anweisungen, um nahezu jeden Aspekt eines Q# Programms zu erstellen, und keine einzelne Seite kann alle Informationen im Zusammenhang mit Ihnen einschließen.
Weitere Informationen zur lexikalischen Struktur und Formatierung finden Sie unter " [ Q# Dateistruktur](xref:microsoft.quantum.guide.filestructure)". Informationen zur Zuweisung und zum Gültigkeitsbereich von Symbol Bindungen finden Sie unter [Variablen in Q# ](xref:microsoft.quantum.guide.variables), und für Ablauf Steuerungs Schleifen wie `for` , siehe [Ablauf Steuerung in Q# ](xref:microsoft.quantum.guide.controlflow).

## <a name="next-steps"></a>Nächste Schritte

Beginnen Sie mit dem Erlernen von [Typen in Q# ](xref:microsoft.quantum.guide.types).

Weitere Hintergrundinformationen zu den Grundlagen und der Motivation dahinter Q# finden [Sie unter Warum brauchen wir Q# ?](https://devblogs.microsoft.com/qsharp/why-do-we-need-q/).

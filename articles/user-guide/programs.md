---
title: 'F #-Einführung'
description: 'Schnelle Einführung in Quantum-Programme in f #'
author: beheim
ms.author: beheim
ms.date: 11/08/2020
ms.topic: article
uid: microsoft.quantum.guide.programs
ms.openlocfilehash: 975bcda5e0042406b465a83f17f1d2d3f5a1ec4f
ms.sourcegitcommit: b930bb59a1ba8f41d2edc9ed98197109aa8c7f1b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96233974"
---
# <a name="q-quantum-programming-language"></a>Q # Quantum-Programmiersprache

Alles, was Sie über die Programmiersprache q # wissen müssen, ist im [f #](xref:microsoft.quantum.qsharp.index)-Programmiersprachen Handbuch ausführlich beschrieben. Wie bei allen anderen ist unser [sprach Entwurfsprozess](https://github.com/microsoft/qsharp-language#q-language-and-core-libraries-design) Open Source, und wir freuen uns auf Beiträge.
Weitere Hintergrundinformationen zu den Grundlagen und der Motivation hinter q # finden [Sie unter Warum benötigen wir q #?](https://devblogs.microsoft.com/qsharp/why-do-we-need-q/).  
Q # wird als Teil des Quantum Development Kit (QDK) bereitgestellt, um eine kurze Übersicht zu erhalten. Weitere Informationen finden Sie unter [Was ist das QDK?](xref:microsoft.quantum.overview.q-sharp). 

## <a name="what-is-a-quantum-program"></a>Was ist ein Quantum-Programm?

Ein Quantum-Programm kann als ein bestimmter Satz klassischer Unterroutinen angesehen werden, die, wenn Sie aufgerufen werden, eine Berechnung durchführen, indem Sie mit einem Quantum-System interagieren. ein in Q # geschriebenes Programm modelliert den Quantenzustand nicht direkt, sondern beschreibt, wie ein klassischer Steuerungscomputer mit Qubits interagiert.
Dies ermöglicht es uns, unabhängig davon, was ein Quantum-Status *ist* , auch auf jedem Zielcomputer zu sein, der je nach Computer unterschiedliche Interpretationen aufweisen kann. 

Eine wichtige Folge davon besteht darin, dass q # nicht in der Lage ist, den Zustand eines Qubit oder anderer Eigenschaften von Quantum-Mechanismen direkt zu überprüfen, was sicherstellt, dass ein q #-Programm physisch auf einem Quantum-Computer ausgeführt werden kann.
Stattdessen kann ein Programm Vorgänge wie z. b [`Measure`](xref:Microsoft.Quantum.Intrinsic.Measure) . verwenden, um klassische Informationen aus einem Qubit zu extrahieren.

Nach dem zuordnen kann ein Qubit an Vorgänge und Funktionen weitergegeben werden, die auch als *callables* bezeichnet werden. In gewisser Hinsicht ist dies alles, was ein Q #-Programm mit einem Qubit tun kann. Alle direkten Aktionen für den Zustand eines Qubit werden alle durch *intrinsische* callables definiert, [`X`](xref:Microsoft.Quantum.Intrinsic.X) wie [`H`](xref:Microsoft.Quantum.Intrinsic.H) z. b. und, d. h. Aufrufe, deren Implementierungen nicht in Q # definiert sind, sondern stattdessen vom Zielcomputer definiert werden. Diese Vorgänge *werden tatsächlich nur* vom Zielcomputer durchgeführt, mit dem das jeweilige Q #-Programm ausgeführt wird.

Wenn Sie das Programm z. b. in unserem [vollständigen Simulator](xref:microsoft.quantum.machines.full-state-simulator)ausführen, führt der Simulator die entsprechenden mathematischen Operationen für das simulierte Quantum-System aus.
Wenn der Zielcomputer jedoch ein echter Quantum-Computer ist, wird der Quantum-Computer durch das aufrufen solcher Vorgänge in Q # an die Zukunft weitergeleitet, um die entsprechenden *echten* Vorgänge auf dem *realen* Quantum-System auszuführen (z. b. genau zeitgesteuerte Laserpulse).

Ein Q #-Programm kombiniert diese Vorgänge neu, wie von einem Zielcomputer definiert, um neue Vorgänge auf höherer Ebene zu erstellen, um die Quantum-Berechnung auszudrücken.
Auf diese Weise vereinfacht f # das Ausdrücken der Logik zugrunde liegenden Quantum-und Hybrid-Quantum – klassische Algorithmen und ist gleichzeitig in Bezug auf die Struktur eines Ziel Computers oder Simulators allgemein.

Ein einfaches Beispiel ist das folgende Programm, das ein Qubit im $ \ket $-Zustand zuordnet {0} , dann einen Hadamard-Vorgang `H` darauf anwendet und das Ergebnis in der `PauliZ` Basis misst.

```qsharp
@EntryPoint()
operation MeasureOneQubit() : Result {
    // The following using block creates a fresh qubit and initializes it
    // in the |0〉 state.
    using (qubit = Qubit()) {
        // We apply a Hadamard operation H to the state, thereby preparing the
        // state 1 / sqrt(2) (|0〉 + |1〉).
        H(qubit);
        // Now we measure the qubit in Z-basis.
        let result = M(qubit);
        // As the qubit is now in an eigenstate of the measurement operator,
        // we reset the qubit before releasing it.
        if (result == One) { X(qubit); }
        // Finally, we return the result of the measurement.
        return result;
    }
}
```

Unsere [Quantum-Katas](https://github.com/microsoft/QuantumKatas#introduction) sind eine gute Einführung in die [Quantum Computing-Konzepte](https://github.com/microsoft/QuantumKatas#quantum-computing-concepts-qubits-and-gates) , wie z. b. häufige Quantum-Vorgänge und das Bearbeiten von Qubits. Weitere Beispiele finden Sie auch in systeminternen [Vorgängen und Funktionen](xref:microsoft.quantum.libraries.standard.prelude).




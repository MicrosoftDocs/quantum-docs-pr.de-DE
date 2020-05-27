---
title: Einführung in die Quanten-Katas
description: Erfahren Sie mehr über die Katas (Schulungsübungen), die zum Microsoft Quantum Development Kit (QDK) gehören
author: natke
ms.author: nakersha
ms.date: 10/17/2019
ms.topic: overview
uid: microsoft.quantum.overview.katas
ms.openlocfilehash: 204033c81b1f6d05c255170ee5662ce9388c3dbf
ms.sourcegitcommit: 328f45a0b64cb6b325fa9d3b3ddb74a6a7a97ee9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/19/2020
ms.locfileid: "83660752"
---
# <a name="learn-quantum-computing-with-the-quantum-katas"></a>Erlernen des Quantencomputings mit den Quanten-Katas

Bei den [Quanten-Katas](https://github.com/Microsoft/QuantumKatas/) handelt es sich um eine Open Source-Sammlung mit eigenverantwortlich zu absolvierenden Tutorials und Programmierübungen mit dem Ziel, Ihnen gleichzeitig Elemente des Quantencomputings und der Q#-Programmierung zu vermitteln.

## <a name="learning-by-doing"></a>Learning by Doing

In den in diesem Projekt enthaltenen Tutorials und Übungen geht es um „Learning by Doing“: Sie enthalten Programmieraufgaben zu bestimmten Themen, die von „Sehr einfach“ bis zu „Sehr anspruchsvoll“ reichen. Für jede Aufgabe müssen Sie etwas Code einfügen. Für die ersten Aufgaben ist vielleicht nur eine Zeile erforderlich, während Sie später ggf. ein größeres Stück Code bereitstellen müssen.

Am wichtigsten ist Folgendes: Die Katas umfassen auch Testframeworks, mit denen die Lösungen für die Aufgaben eingerichtet, ausgeführt und überprüft werden. Auf diese Weise erhalten Sie sofort Feedback zu Ihrer Lösung und können Ihren Ansatz überdenken, falls er nicht korrekt ist.

Sie können die Katas zum Lernen in der Umgebung Ihrer Wahl verwenden:

* Jupyter-Notebooks online innerhalb der Binder-Umgebung
* Jupyter-Notebooks, die auf Ihrem lokalen Computer ausgeführt werden
* Visual Studio
* Visual Studio Code

## <a name="what-can-i-learn-with-the-quantum-katas"></a>Was kann ich mit den Quanten-Katas lernen?

Hier ist eine Zusammenfassung der wichtigsten Themen angegeben, die durch die Quanten-Katas abgedeckt werden. Wir empfehlen Ihnen, am Anfang diesem Lernpfad zu folgen. So können Sie sicherstellen, dass Sie ausreichend mit den grundlegenden Konzepten des Quantencomputings vertraut sind. Sie können natürlich die Themen überspringen, mit denen Sie sich gut auskennen, z. B. komplexe Arithmetik, und die Algorithmen in der von Ihnen gewünschten Reihenfolge erlernen.

### <a name="introduction-to-quantum-computing-concepts"></a>Einführung in die Konzepte des Quantencomputings

* [Komplexe Arithmetik](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/ComplexArithmetic)
* [Lineare Algebra](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/LinearAlgebra)
* [Das Konzept eines Qubits](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/Qubit)
* [Quantengatter mit einem einzelnen Qubit](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/SingleQubitGates)
* [Systeme mit mehreren Qubits](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/MultiQubitSystems)
* [Gates mit mehreren Qubits](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/MultiQubitGates)

### <a name="quantum-computing-fundamentals"></a>Grundlagen des Quantencomputings

* [Erkennen von Quantengattern](https://github.com/microsoft/QuantumKatas/tree/master/BasicGates)
* [Erstellen einer Quantenüberlagerung](https://github.com/microsoft/QuantumKatas/tree/master/Superposition)
* [Unterscheiden von Quantenzuständen mit Messungen](https://github.com/microsoft/QuantumKatas/tree/master/Measurements)
* [Verknüpfte Messungen](https://github.com/microsoft/QuantumKatas/tree/master/JointMeasurements)

### <a name="algorithms"></a>Algorithmen

* [Quantenteleportation](https://github.com/microsoft/QuantumKatas/tree/master/Teleportation)
* [Superdichte Codeerstellung](https://github.com/microsoft/QuantumKatas/tree/master/SuperdenseCoding)
* [Deutsch-Jozsa-Algorithmus](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/ExploringDeutschJozsaAlgorithm)
* [Implementieren des Algorithmus für die Grover-Suche](https://github.com/microsoft/QuantumKatas/tree/master/GroversAlgorithm)
* [Untersuchen allgemeiner Eigenschaften des Algorithmus für die Grover-Suche](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/ExploringGroversAlgorithm)
* Lösen realer Probleme mit dem Grover-Algorithmus: [SAT-Probleme](https://github.com/microsoft/QuantumKatas/tree/master/SolveSATWithGrover) und [Probleme mit der farbigen Kennzeichnung von Graphen](https://github.com/microsoft/QuantumKatas/tree/master/GraphColoring)

### <a name="protocols-and-libraries"></a>Protokolle und Bibliotheken

* [BB84-Protokoll für Quantenschlüsselverteilung](https://github.com/microsoft/QuantumKatas/tree/master/KeyDistribution_BB84)
* Quantenfehlerkorrektur: [Korrekturcode für Bitkipper](https://github.com/microsoft/QuantumKatas/tree/master/QEC_BitFlipCode)
* [Phasenschätzung](https://github.com/microsoft/QuantumKatas/blob/master/PhaseEstimation)
* Quantenarithmetik: [Erstellen von Ripple-Carry-Addierern](https://github.com/microsoft/QuantumKatas/blob/master/RippleCarryAdder)

### <a name="entanglement-games"></a>Verschränkungsspiele

* [Spiel „CHSH“](https://github.com/microsoft/QuantumKatas/tree/master/CHSHGame)
* [Spiel „GHZ“](https://github.com/microsoft/QuantumKatas/tree/master/GHZGame)
* [Spiel „Magisches Mermin-Peres-Quadrat“](https://github.com/microsoft/QuantumKatas/tree/master/MagicSquareGame)

## <a name="resources"></a>Ressourcen

* Die gesamte Serie der [Quanten-Katas](https://github.com/microsoft/QuantumKatas) ansehen
* [Onlineausführung der Katas](https://aka.ms/try-quantum-katas)

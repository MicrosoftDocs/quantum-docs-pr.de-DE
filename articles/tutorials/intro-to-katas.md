---
title: Einführung in die Quanten-Katas
description: Erfahren Sie mehr über die Katas (Schulungsübungen), die zum Microsoft Quantum Development Kit (QDK) gehören
author: bradben
ms.author: v-benbra
ms.date: 06/02/2020
ms.topic: overview
uid: microsoft.quantum.overview.katas
no-loc:
- Q#
- $$v
ms.openlocfilehash: 097d7f70088b6ee84a1e91ee99be59149dd9e15b
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/21/2020
ms.locfileid: "90834821"
---
# <a name="learn-quantum-computing-with-the-quantum-katas"></a>Erlernen des Quantencomputings mit den Quanten-Katas

[Die Quantum-Katas](https://github.com/Microsoft/QuantumKatas/) sind Open Source-Lernprogramme und programmierübungen, die darauf abzielen, die Elemente von Quantum Computing und Q# Programmieren gleichzeitig zu unterrichten.

## <a name="learning-by-doing"></a>Learning by Doing

In den in diesem Projekt enthaltenen Tutorials und Übungen geht es um „Learning by Doing“: Sie enthalten Programmieraufgaben zu bestimmten Themen, die von „Sehr einfach“ bis zu „Sehr anspruchsvoll“ reichen. Für jede Aufgabe müssen Sie etwas Code einfügen. Für die ersten Aufgaben ist vielleicht nur eine Zeile erforderlich, während Sie später ggf. ein größeres Stück Code bereitstellen müssen.

Am wichtigsten ist, dass die Katas Test-Frameworks umfasst, die die Projektmappen einrichten, ausführen und validieren. Auf diese Weise erhalten Sie sofort Feedback zu Ihrer Lösung und können Ihren Ansatz überdenken, falls er nicht korrekt ist.

Sie können Katas zum Erlernen in Ihrer bevorzugten Umgebung verwenden:

* Jupyter-Notebooks online innerhalb der Binder-Umgebung
* Jupyter-Notebooks, die auf Ihrem lokalen Computer ausgeführt werden
* Visual Studio
* Visual Studio Code

## <a name="what-can-i-learn-with-the-quantum-katas"></a>Was kann ich mit den Quanten-Katas lernen?

Entdecken Sie die Grundlagen und Grundlagen von Quantum Computing, oder vertiefen Sie die Quantum-Algorithmen und-Protokolle. Wir empfehlen Ihnen, am Anfang diesem Lernpfad zu folgen. So können Sie sicherstellen, dass Sie ausreichend mit den grundlegenden Konzepten des Quantencomputings vertraut sind. Sie können natürlich die Themen überspringen, mit denen Sie sich gut auskennen, z. B. komplexe Arithmetik, und die Algorithmen in der von Ihnen gewünschten Reihenfolge erlernen.

### <a name="introduction-to-quantum-computing-concepts"></a>Einführung in die Konzepte des Quantencomputings

| Ausbreiten | BESCHREIBUNG |
|:-----|-------------|
|[Komplexe Arithmetik](https://github.com/microsoft/QuantumKatas/tree/main/tutorials/ComplexArithmetic)|In diesem Tutorial wird ein Teil des mathematischen Hintergrunds erläutert, der zum Arbeiten mit Quantum Computing erforderlich ist, z. b. imaginäre und komplexe Zahlen.|
|[Lineare Algebra](https://github.com/microsoft/QuantumKatas/tree/main/tutorials/LinearAlgebra)|Lineare Algebra wird zur Darstellung von Quantum-Zuständen und-Vorgängen in Quantum Computing verwendet. Dieses Tutorial behandelt die Grundlagen, einschließlich Matrizen und Vektoren.|
|[Das Konzept eines Qubits](https://github.com/microsoft/QuantumKatas/tree/main/tutorials/Qubit)|Erfahren Sie mehr über Qubits-eines der Kernkonzepte von Quantum Computing. |
|[Quantengatter mit einem einzelnen Qubit](https://github.com/microsoft/QuantumKatas/tree/main/tutorials/SingleQubitGates)|In diesem Tutorial werden Single-Qubit-Quantum-Gates vorgestellt, die als Bausteine von Quantum-Algorithmen fungieren und Quantum-Qubit-Zustände auf verschiedene Weise transformieren.|
|[Systeme mit mehreren Qubits](https://github.com/microsoft/QuantumKatas/tree/main/tutorials/MultiQubitSystems)|In diesem Tutorial werden multiqubit-Systeme, ihre Darstellung in mathematischer Notation und Q# Code sowie das Konzept von entanglement vorgestellt.|
|[Multi-Qubit-Quantum-Gates](https://github.com/microsoft/QuantumKatas/tree/main/tutorials/MultiQubitGates)|Dieses Tutorial folgt dem Tutorial zu [Single-Qubit Quantum Gates](https://github.com/microsoft/QuantumKatas/tree/main/tutorials/SingleQubitGates) und konzentriert sich auf das Anwenden von Quantum-Gates auf multiqubit-Systeme.|

### <a name="quantum-computing-fundamentals"></a>Grundlagen des Quantencomputings

| Ausbreiten | BESCHREIBUNG |
|:-----|-------------|
|[Erkennen von Quantengattern](https://github.com/microsoft/QuantumKatas/tree/main/BasicGates)|Eine Reihe von Übungen, mit denen Sie sich mit den grundlegenden Quantum Gates in vertraut machen können Q# . Umfasst Übungen für einfache Single-Qubit-und Multi-Qubit-Gates, Adjoint und gesteuerte Gates und die Verwendung von Gates zum Ändern des Status eines Qubit.|
|[Erstellen einer Quantenüberlagerung](https://github.com/microsoft/QuantumKatas/tree/main/Superposition)|Verwenden Sie diese Übungen, um sich mit dem Konzept der superposition und der Programmierung in vertraut zu machen Q# . Umfasst Übungen für einfache Single-Qubit-und Multi-Qubit-Gates, superposition und Fluss Steuerung sowie Rekursion in Q# .|
|[Unterscheiden von Quantenzuständen mit Messungen](https://github.com/microsoft/QuantumKatas/tree/main/Measurements)|Lösen Sie diese Übungen, und lernen Sie die Quanten Messung und orthogonale und nicht orthogonale Zustände kennen. |
|[Verknüpfte Messungen](https://github.com/microsoft/QuantumKatas/tree/main/JointMeasurements)|Erfahren Sie mehr über gemeinsame Paritäts Messungen und wie Sie den [Measure](xref:microsoft.quantum.intrinsic.measure) -Vorgang zum unterscheiden von Quantum-Zuständen verwenden|

### <a name="algorithms"></a>Algorithmen

| Ausbreiten | BESCHREIBUNG |
|:-----|-------------|
|[Quantenteleportation](https://github.com/microsoft/QuantumKatas/tree/main/Teleportation)|Diese Kata untersucht Quantum-Teleportation: ein Protokoll, das die Kommunikation eines Quantum-Zustands mithilfe der klassischen Kommunikation und zuvor freigegebenen Quantum-Entanglement ermöglicht.|
|[Superdichte Codeerstellung](https://github.com/microsoft/QuantumKatas/tree/main/SuperdenseCoding)|Superdense Coding ist ein Protokoll, das die Übertragung von zwei klassischen Informationen ermöglicht, indem nur ein Qubit mithilfe der zuvor freigegebenen Quantum-Entanglement gesendet wird.  |
|[Deutsch-Jozsa-Algorithmus](https://github.com/microsoft/QuantumKatas/tree/main/tutorials/ExploringDeutschJozsaAlgorithm)|Dieser Algorithmus ist für eines der ersten Beispiele eines Quantum-Algorithmus bekannt, der exponentiell schneller ist als ein beliebiger deterministischer klassischer Algorithmus.|
|[Untersuchen allgemeiner Eigenschaften des Algorithmus für die Grover-Suche](https://github.com/microsoft/QuantumKatas/tree/main/tutorials/ExploringGroversAlgorithm)|Eine allgemeine Einführung in einen der bekanntesten Algorithmen in Quantum Computing. Dadurch wird das Problem beim Auffinden einer Eingabe in ein schwarzes Feld (Oracle) gelöst, das eine bestimmte Ausgabe erzeugt. |
|[Implementieren des Algorithmus für die Grover-Suche](https://github.com/microsoft/QuantumKatas/tree/main/GroversAlgorithm)|Diese Kata geht tiefer in den Suchalgorithmus von Grover ein und deckt das Schreiben von Oracles, das Durchführen von Schritten des Algorithmus und schließlich das Fortsetzen des Vorgangs.|
|[Lösen realer Probleme mit dem Algorithmus von Grover: Sat-Probleme](https://github.com/microsoft/QuantumKatas/tree/main/SolveSATWithGrover)|Eine Reihe von Übungen, die den Algorithmus von Grover zum lösen realistischer Probleme mithilfe von [booleschen satismoability-Problemen](https://en.wikipedia.org/wiki/Boolean_satisfiability_problem) (Sat) als Beispiel verwendet.  |
|[Lösen realer Probleme mithilfe des Algorithmus "Grover": Graph-Farbgebung](https://github.com/microsoft/QuantumKatas/tree/main/GraphColoring)| Diese Kata erläutert den Algorithmus von Grover, dieses Mal, um [Probleme](https://en.wikipedia.org/wiki/Constraint_satisfaction_problem)mit der Einschränkungs Zufriedenheit zu lösen, mithilfe eines Diagramms als Beispiel. |

### <a name="protocols-and-libraries"></a>Protokolle und Bibliotheken

| Ausbreiten | BESCHREIBUNG |
|:-----|-------------|
|[BB84-Protokoll für Quantenschlüsselverteilung](https://github.com/microsoft/QuantumKatas/tree/main/KeyDistribution_BB84)|Erfahren Sie, wie Sie ein Quantum Key Distribution-Protokoll, [BB84](https://en.wikipedia.org/wiki/BB84), mit Qubits zum Austauschen von Kryptografieschlüsseln verwenden und implementieren. |
|[Fehler beim Korrigieren des Codes durch bitkippen](https://github.com/microsoft/QuantumKatas/tree/main/QEC_BitFlipCode)|Erkunden Sie die Quantum-Fehlerkorrektur mit dem einfachsten der QEC-Codes (Quantum Error-Correction), dem drei-Qubit-bitflip-Code.|
|[Phasenschätzung](https://github.com/microsoft/QuantumKatas/blob/main/PhaseEstimation)|Phasen Schätz Algorithmen sind einige der grundlegendsten Bausteine von Quantum Computing. Erfahren Sie mehr über die Phasen Schätzung mit diesen Übungen, die die Quantum-Phasen-Schätzung abdecken und wie Phasen-Schätz Routinen in vorbereitet und ausgeführt werden Q# .|
|[Quantum-Arithmetik: Entwickeln von Ripple-Carry-addern](https://github.com/microsoft/QuantumKatas/blob/main/RippleCarryAdder)|Eine ausführliche Reihe von Übungen, mit denen die Addition von [Ripple](https://en.wikipedia.org/wiki/Adder_(electronics)#Ripple-carry_adder) auf einem Quantum-Computer untersucht wird. Erstellen Sie einen direkten Quantum-Adder, erweitern Sie ihn mit einem anderen Algorithmus, und erstellen Sie abschließend einen direkten Quantum-subtraktor.   |

### <a name="entanglement-games"></a>Verschränkungsspiele

| Ausbreiten | BESCHREIBUNG |
|:-----|-------------|
|[Spiel „CHSH“](https://github.com/microsoft/QuantumKatas/tree/main/CHSHGame)|Erkunden Sie Quantum jede Verflechtungen mit einer Implementierung des [CHSH](https://en.wikipedia.org/wiki/CHSH_inequality) -Spiels. Dieses [nicht lokale](https://en.wikipedia.org/wiki/Quantum_refereed_game) Spiel zeigt, wie die Wahrscheinlichkeit von Quantum jede Verflechtungen verwendet werden kann, um die Wahrscheinlichkeit zu erhöhen, dass über das, was mit einer reinen klassischen Strategie möglich wäre, gewonnen wird.|
|[Spiel „GHZ“](https://github.com/microsoft/QuantumKatas/tree/main/GHZGame)|Das GHz-Spiel ist ein weiteres nicht lokales Spiel, das jedoch drei Spieler umfasst.|
|[Spiel „Magisches Mermin-Peres-Quadrat“](https://github.com/microsoft/QuantumKatas/tree/main/MagicSquareGame)|Eine Reihe von Übungen, die [Quantum-Pseudo teleblohe](https://en.wikipedia.org/wiki/Quantum_pseudo-telepathy#The_Mermin%E2%80%93Peres_magic_square_game) zum Lösen eines magischen quadratischen Spiels untersucht.  |

## <a name="resources"></a>Ressourcen

Die gesamte Serie der [Quanten-Katas](https://github.com/microsoft/QuantumKatas) ansehen

[Onlineausführung der Katas](https://aka.ms/try-quantum-katas)

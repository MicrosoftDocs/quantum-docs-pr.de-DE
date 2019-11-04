---
title: Glossar | Microsoft-Dokumentation
description: Glossar mit Quantum-Begriffen
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.glossary
ms.openlocfilehash: bfa275b3330ea2c2a541b08f137893b63b6213aa
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/26/2019
ms.locfileid: "73183623"
---
|Laufzeit|Definition|
|-------------|----------|
|Adjoint|Die komplexe konjugierte, die den Vorgang übertragen hat. Bei Vorgängen, die einen einheitlichen Operator implementieren, ist das Adjoint das Gegenteil des Vorgangs.|
|Callable|Vorgänge und Funktionen werden zusammen als *callables*bezeichnet.|
|Standard|In Q # definierte Vorgänge und Funktionen, die auf der in der Einleitung definierten Logik aufbauen. Die Implementierung der Standardbibliothek ist in Bezug auf die Zielcomputer agnostisch.|
|Clifford-Gruppe|Der Satz von Vorgängen, die die oktanten der Bloch-Kugel belegen. Hierzu gehören: `X`, `Y`, `Z`, `H` und `S`|
|Klimatisiert|Ein Quantum-Vorgang, der ein oder mehrere Qubits als Enabler für den Ziel Vorgang annimmt.|
|Dirac-Notation|Eine kurz Darstellung des Quantums. Weitere Informationen finden Sie im Abschnitt [Dirac-Notation](xref:microsoft.quantum.concepts.dirac) .|
|Eigenwerte und Eigenvektoren|Weitere Informationen finden Sie im [Abschnitt Erweiterte Matrix](xref:microsoft.quantum.concepts.matrix-advanced) .|
|EPR-paar|Wird auch als [Glocken Zustand](https://en.wikipedia.org/wiki/Bell_state) bezeichnet.|
|Entwicklungs|Wie sich der Status im Laufe der Zeit ändert. Ein Beispiel finden Sie im Abschnitt <xref:microsoft.quantum.concepts.matrix-advanced#matrix-exponentials>. |
|Funktion|Rein klassische Routinen in der Q #-Sprache|
| <a id="global-phase"></a>Globale Phase | Zwei Zustände, die bis zu einem Vielfachen einer komplexen Zahl $e ^ {i\phi} $ identisch sind, werden bis zu einer globalen Phase unterschieden. Im Gegensatz zu lokalen Phasen können globale Phasen nicht durch eine beliebige Messung beobachtet werden. Weitere Informationen finden Sie unter [Pauli-Messungen](xref:microsoft.quantum.concepts.pauli) . |
|Messung|Abrufen eines klassischen Bits aus einem Qubit (oder einem Satz von Qubits). Weitere Informationen finden Sie im Abschnitt mit den [Qubit-Konzepten](xref:microsoft.quantum.concepts.qubit) .|
|Veränderlich|Eine Variable, deren Wert geändert werden kann, nachdem Sie erstellt wurde.|
|Namespace|Eine Bezeichnung für eine Auflistung verwandter Namen (in der Regel Vorgänge, Funktionen und Typen). Beispielsweise benennt der Namespace [`Microsoft.Quantum.Preparation`](xref:microsoft.quantum.preparation) alle Symbole, die in der Standardbibliothek definiert sind und bei der Vorbereitung von anfänglichen Zuständen helfen.|
|Vorgang|Die grundlegende Einheit der Quantum-Ausführung in Q #. Dies entspricht ungefähr einer Funktion in C oder C++ oder python oder einer statischen Methode in C# oder Java.|
|Operator Anwendung|Ausführen eines Quantum-Vorgangs. Dadurch wird in der Regel eine einheitliche Matrix auf den aktuellen Status Vektor angewendet. Weitere Details finden [Sie unter Einführung in Quantum Concepts](xref:microsoft.quantum.concepts.intro) .|
|Oracle|Eine Unterroutine, die zur Laufzeit Daten abhängige Informationen für einen Quantum-Algorithmus bereitstellt. In der Regel besteht das Ziel darin, eine Superposition der Ausgaben bereitzustellen, die den Eingaben in der superposition entsprechen.   |
|Partielle Anwendung|Aufrufen einer Funktion oder eines Vorgangs ohne alle erforderlichen Parameter. Der gibt eine neue Aufruf Bare zurück, die nur die fehlenden Parameter benötigt, die während einer zukünftigen Anwendung bereitgestellt werden.|
|Pauli-Operatoren|Die `X`, `Y` und `Z` Quantum Gates.|
|Einleitung|Der Satz primitiver und klassischer Vorgänge und Funktionen, die von jedem einzelnen Zielcomputer definiert werden, und nicht auf der Q #-Ebene.|
|Quantum-Leitung|Die Darstellung eines Programms für einen Quantum-Computer. Weitere Informationen finden Sie im Abschnitt <xref:microsoft.quantum.concepts.circuits>.|
|Quantum-Status|Eine Darstellung der Qubits im System. Dies wird in der Regel als komplexer Spalten Vektor bezeichnet. Weitere Informationen finden Sie unter <xref:microsoft.quantum.concepts.vectors>. |
|Qubit|Einheit des Quantum-Speichers. Weitere Informationen finden Sie im Abschnitt <xref:microsoft.quantum.concepts.qubit>.|
|Wiederholung-bis-Erfolg|Ein Quantum-Algorithmus, der probabilistisch erfolgreich ist. Bei einem Fehler wird die Routine wiederholt, bis Sie erfolgreich ist (oder ein Grenzwert erreicht wurde). |
|Software Stapel|Der gesamte Satz klassischer und quantener Software sowie die Compiler, Simulatoren und Laufzeiten, die für den Betrieb eines Quantum-Computers erforderlich sind. Weitere Informationen finden Sie im Abschnitt <xref:microsoft.quantum.concepts.software-stack>. |
|Zielcomputer|Ein Kompilierungs Ziel, das ein abstraktes Quantum-Programm auf Hardware oder Simulation senkt. Dies schließt in der Regel Umschreib Vorgänge für viele Zwecke ein, einschließlich Gate-Ersetzung, Codierung für die Fehlerkorrektur, geometrisches Layout und andere.|
|Tupel|Durch Kommas getrennte Typen, die über Klammern gruppiert sind. |
|Benutzerdefinierter Typ|Sammlung integrierter oder zuvor definierter Typen, die als einzelne Einheit bezeichnet werden können.|


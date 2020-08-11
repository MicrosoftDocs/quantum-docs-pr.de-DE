---
title: Quantencomputer und -simulatoren
description: Hier finden Sie Informationen zu Quantenhardware und Quantensimulatoren sowie zur Funktionsweise von Quantenoperationen.
author: bradben
ms.author: bradben
ms.date: 5/5/2020
ms.topic: overview
uid: microsoft.quantum.overview.simulators
no-loc:
- Q#
- $$v
ms.openlocfilehash: 299baea75865a4f0ece6b490cef3301dd2a672ac
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2020
ms.locfileid: "87867708"
---
# <a name="quantum-computers-and-quantum-simulators"></a>Quantencomputer und -simulatoren

Die Entwicklung von Quantencomputern steckt noch in den Kinderschuhen. Hardware und Wartung sind teuer, und die meisten Systeme befinden sich in Universitäten und Forschungslabors. Die Entwicklung der Technologie schreitet jedoch voran, und inzwischen ist eingeschränkter öffentlicher Zugriff auf einige Systeme verfügbar.

Bei Quantensimulatoren handelt es sich um Softwareprogramme, die auf klassischen Computern ausgeführt werden und das Ausführen und Testen von Quantenprogrammen in einer Umgebung ermöglichen, die die Reaktion von Qubits auf verschiedene Operationen vorhersagt.

## <a name="quantum-hardware"></a>Quantenhardware

Ein Quantencomputer besteht aus drei Hauptkomponenten: einem Bereich für die Qubits, einer Methode für die Signalübertragung an die Qubits sowie einem klassischen Computer zum Ausführen eines Programms und zum Senden von Anweisungen.

- Das für Qubits verwendete Quantenmaterial ist fragil und höchst empfindlich gegenüber Umwelteinflüssen. Bei einigen Methoden zur Speicherung von Qubits wird die Einheit, die die Qubits enthält, auf eine Temperatur knapp über dem absoluten Nullpunkt gekühlt, um die Kohärenz zu maximieren. Bei anderen Arten von Einheiten für Qubits wird eine Vakuumkammer verwendet, um Schwingungen zu minimieren und die Qubits zu stabilisieren.  
- Signale können auf verschiedene Weise an die Qubits gesendet werden – etwa mithilfe von Mikrowellen, per Laser oder mittels Stromspannung.

Damit ein Quantencomputer ordnungsgemäß funktioniert, muss eine Vielzahl von Herausforderungen bewältigt werden. Die Fehlerkorrektur ist bei Quantencomputern ein erhebliches Problem, und die Fehlerrate erhöht sich mit zunehmender Qubit-Anzahl (also beim Hochskalieren). Aufgrund dieser Einschränkungen sind wir noch weit von einem Quanten-PC für den eigenen Schreibtisch entfernt. Ein für kommerzielle Zwecke geeigneter und in einer Laborumgebung betriebener Quantencomputer ist allerdings bereits vorstellbar.

## <a name="quantum-simulators"></a>Quantensimulatoren

Mit auf klassischen Computern ausgeführten Quantensimulatoren lässt sich das Ausführen von Quantenalgorithmen auf einem Quantensystem simulieren.  Das Quantum Development Kit (QDK) von Microsoft enthält einen Vektorsimulator für den vollständigen Zustand sowie weitere spezialisierte Quantensimulatoren.

## <a name="topological-qubit"></a>Topologisches Qubit

Microsoft entwickelt einen Quantencomputer auf der Grundlage topologischer Qubits. Ein topologisches Qubit wird weniger durch Veränderungen in seiner Umgebung beeinflusst, was das Maß an erforderlicher externer Fehlerkorrektur verringert.

Topologische Qubits zeichnen sich durch erhöhte Stabilität und Widerstandsfähigkeit gegenüber Umgebungsrauschen aus, was bedeutet, dass sie sich leichter skalieren lassen und länger zuverlässig bleiben.

## <a name="microsoft-and-quantum-hardware-partnerships"></a>Microsoft und Partnerschaften für Quantenhardware

Microsoft arbeitet mit den Quantenhardwareherstellern IonQ, Honeywell und QCI zusammen, um Entwicklern in Zukunft den Zugriff auf Quantencomputer zu ermöglichen. Über die Azure Quantum-Plattform können Entwickler das Quantum Development Kit (QDK) von Microsoft sowie Q# verwenden, um Quantenprogramme zu schreiben und remote auszuführen.

## <a name="quantum-computations"></a>Quantenberechnungen

Das Ausführen von Berechnungen auf einem Quantencomputer oder in einem Quantensimulator basiert auf einem einfachen Prozess:

- Zugreifen auf die Qubits
- Initialisieren der Qubits, sodass sie den gewünschten Zustand aufweisen
- Durchführen von Operationen, um die Zustände der Qubits zu transformieren
- Messen der neuen Zustände der Qubits

Für die Initialisierung und Transformierung von Qubits werden **Quantenoperationen** (manchmal auch als Quantengatter bezeichnet) verwendet. Quantenoperationen sind vergleichbar mit Logikoperationen aus dem klassischen Computing (beispielsweise AND, OR, NOT oder XOR). Die Komplexität reicht dabei von einfachen Operationen (etwa im Falle eines Qubits, dessen Zustand von 1 in 0 geändert wird, oder im Falle der Verschränkung eines Qubit-Paars) bis hin zur Verwendung einer Reihe von Operationen, um die Wahrscheinlichkeit eines bestimmten Ergebnisses beim Kollaps eines superponierten Qubits zu beeinflussen.

> [!NOTE] 
> Die [Q#-Bibliotheken](xref:microsoft.quantum.libraries) enthalten integrierte Operationen, die komplexe Kombinationen von untergeordneten Quantenoperationen definieren. Mithilfe der Bibliotheksoperationen können Sie Qubits transformieren und komplexere benutzerdefinierte Operationen erstellen.  

Die Messung des Ergebnisses der Berechnung liefert zwar eine Antwort, bei einigen Quantenalgorithmen ist das aber nicht unbedingt die richtige Antwort. Da das Ergebnis einiger Quantenalgorithmen auf der Wahrscheinlichkeit basiert, die durch die Quantenoperationen konfiguriert wurde, werden diese Berechnungen mehrmals ausgeführt, um eine Wahrscheinlichkeitsverteilung zu erhalten und die Genauigkeit der Ergebnisse zu optimieren.  Die Gewissheit, dass eine Operation eine korrekte Antwort geliefert hat, wird als Quantenverifizierung bezeichnet und ist eine erhebliche Herausforderung beim Quantencomputing.

## <a name="summary"></a>Zusammenfassung

Beim Quantencomputing werden zum Teil die gleichen Konzepte genutzt wie beim klassischen Computing, es kommen jedoch auch einige neue Dinge hinzu. Im Anschluss finden Sie noch einmal einige wichtige Punkte:

- Quantenhardware ist teuer und empfindlich, weshalb zum Schreiben und Testen von Programmen Quantensimulatoren verwendet werden.
- Sowohl klassische Computer als auch Quantencomputer nutzen Logikoperationen (oder -gatter) zur Vorbereitung von Berechnungen.
- Bei Quantenberechnungen werden Wahrscheinlichkeiten zurückgegeben.

Fortschritte bei der Quantenhardware und bei Quantentechniken führen zu schnellen Veränderungen in diesem Bereich. Informationen zu einigen aktuellen Entwicklungen finden Sie [hier](https://phys.org/search/?search=quantum+computer&s=0).

## <a name="next-steps"></a>Nächste Schritte

[Was sind die Programmiersprache Q# und das QDK?](xref:microsoft.quantum.overview.q-sharp)

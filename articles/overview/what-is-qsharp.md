---
title: Was sind Q# und das QDK?
description: Erfahren Sie mehr über Q#, eine von Microsoft geschaffene Programmiersprache zum Entwickeln von Anwendungen für Quantencomputer und eine Hauptkomponente des Quantum Development Kit von Microsoft.
author: natke
ms.author: nakersha
ms.date: 10/22/2019
ms.topic: article
uid: microsoft.quantum.overview.qsharp
ms.openlocfilehash: a4bf21887e34ac85f75e5e0b9a033138464fd09d
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907000"
---
# <a name="what-are-q-and-the-qdk"></a>Was sind Q# und das QDK?

Q# ist eine Programmiersprache mit Features, die speziell für die Verwendung mit Quantencomputing entwickelt wurden.
Als Hauptkomponente des Quantum Development Kit (QDK) von Microsoft bietet es Quantenprogrammierern ein Framework, das es Ihnen erlaubt, sich auf die Algorithmen zu konzentrieren, ohne sich um technische Details wie die Optimierung von Gattersequenzen oder die physische Implementierung eines Quantencomputers kümmern zu müssen.

Das QDK umfasst eine Vielzahl von Tools, die Entwicklern alles an die Hand geben, was sie benötigen, um mit dem Schreiben von Quantenprogrammen zu beginnen.
Neben der Sprache Q# umfasst das QDK Folgendes:
* die *Q#-Bibliotheken*, die es den Entwicklern ermöglichen, sofort mit der Arbeit zu beginnen und reale Quantenanwendungen zu erstellen
* verschiedene *Zielcomputer*, auf denen Q#-Programme ausgeführt werden können Hierzu zählen auch Ressourcenschätzfunktionen und Simulatoren für größere Quantenprogramme sowie ein Quantensimulator für den vollständigen Zustand, der sich wie ein rauschfreier Quantencomputer verhält. Letzteres ist sehr nützlich, um Ideen zu vermitteln, Programme zu debuggen und mehr über die Quantenphysik zu erfahren, ist allerdings nur für Programme mit relativ wenigen Qubits effizient. Wir freuen uns darauf, die Hardware von Quantencomputern künftig als Zielcomputer verfügbar zu machen.
* *Tools*, um die Arbeit mit Q# so nahtlos wie möglich zu gestalten, wie z. B. Erweiterungen für Visual Studio und VS Code, und Pakete für die Verwendung mit Python und Jupyter Notebooks.
* *API-Dokumentation* für die Kopplung von Q# mit klassischen Hostsprachen wie Python und C#

Anwendungen, die mit dem Quantum Development Kit von Microsoft entwickelt wurden, bestehen in der Regel aus zwei Teilen:
1. Einem oder mehreren Quantenalgorithmen, die mithilfe der Quantenprogrammiersprache Q# implementiert und vom klassischen Hostprogramm aufgerufen werden. Diese bestehen aus 
    - Q#-Vorgängen: Unterroutinen, die Quantenvorgänge enthalten, und 
    - Q#-Funktionen: klassische Unterroutinen, die mit dem Quantenalgorithmus verwendet werden.
2. Einem klassischen Hostprogramm, das in einer klassischen Programmiersprache wie Python oder C# implementiert wurde, das als Haupteinstiegspunkt dient und Q#-Vorgänge aufruft, wenn ein Quantenalgorithmus ausgeführt werden soll.

## <a name="write-quantum-programs-not-quantum-circuits"></a>Schreiben von Quantenprogrammen anstatt Quantenschaltungen

In den Anfängen des Quantencomputings wurden Algorithmen in Form von Diagrammen visualisiert, die den Schaltplänen aus dem klassischen Computing ähnelten.
Zwar hat sich das Schaltungsmodell über viele Jahre als nützlich in der Forschung an Quantencomputing erwiesen, wir bei Microsoft glauben aber, dass Entwickler Quantenschaltungen hinter sich lassen und Quantenalgorithmen und -anwendungen mithilfe von Q# entwickeln können.
Die Sprache Q# wurde entwickelt, um unsere Lehren aus jahrzehntelanger Erfahrung in der klassischen Softwareentwicklung zu nutzen und Quantenentwicklern die Funktionalität höherer Sprachen mit spezieller Ausrichtung auf Quantencomputing an die Hand zu geben.

## <a name="how-does-q-work"></a>Wie funktioniert Q#?

Die Programmiersprache Q# bietet Ihnen intuitive Typen, Operationen und logische Ausdrücke zum Entwickeln von Algorithmen, ohne sich mit der internen Logik des Quantencomputers befassen zu müssen.

Einer der fundamentalen Bausteine von Q# ist der Typ `Qubit`, der nicht kopiert und auf den nicht direkt zugegriffen werden kann, ganz wie ein reales Qubit.
Stattdessen können wir ihn messen und das Ergebnis der Messung in einer `Result`-Variable speichern, einem Q#-Typ, der zwei mögliche Werte annehmen kann: `Zero` und `One`.
Konstrukte wie dieses stellen sicher, dass Algorithmen jederzeit die Gesetze der Quantenphysik beachten und auf Quantencomputern oder Simulatoren ordnungsgemäß ausgeführt werden können.

Q# schließt darüber hinaus Funktionen der klassischen Logik wie Bedingungen und Schleifen mit einer Reihe von Feinheiten ein, um sicherzustellen, dass alle Quantenregeln beachtet werden.
Beispiel: Einschränkung der Art, wie Schleifen ausgeführt werden, um sicherzustellen, dass Quantenvorgänge nicht innerhalb von Funktionen aufgerufen werden, die unter Umständen nur deterministische klassische Unterroutinen enthalten.

Q#-Programme sind häufig mit einem in C# oder Python geschriebenen Hostprogramm gekoppelt, das eine komfortable Organisation von klassischem und Quantencode bieten kann.
Über die Unterstützung von Sprachen wie C# und Python hinaus bietet das QDK mit dem IQ#-Jupyter-Kernel Unterstützung für Jupyter Notebook.

## <a name="what-can-i-use-q-for"></a>Wozu kann ich Q# verwenden?

### <a name="use-q-to-learn-quantum-computing"></a>Verwenden von Q# zum Erlernen von Quantencomputing

Bisher mussten Sie zum Lernen von Quantencomputing das Schaltungsmodell lernen, um die Algorithmen in Form geordneter Sequenzen aus Quantengattern und Messungen zu verstehen. Mit Q# können Sie einen anderen Weg einschlagen: Lernen Sie Quantencomputing durch das Schreiben von Quantenprogrammen.

### <a name="use-q-to-design-quantum-algorithms"></a>Verwenden von Q# zum Entwerfen von Quantenalgorithmen

Q# verfügt über eine wachsende Zahl von Bibliotheken und benutzerdefinierten Typen, mit denen Sie Tools implementieren und erweiterte Quantenalgorithmen erstellen können. Sie müssen beispielsweise zwei Qubits q1 und q2 verschränken? Anstatt einzeln die erforderlichen Gatter anzuwenden, um die Qubits zu verschränken, können Sie die bereits integrierte Operation `PrepareEntangledState([q1], [q2])` verwenden.

### <a name="use-q-to-estimate-quantum-resources"></a>Verwenden von Q# zum Schätzen von Quantenressourcen

Sie können die Ausführung Ihres Q#-Programms simulieren, indem Sie den Quantensimulator für Zustände verwenden, der im Quantum Development Kit (QDK) enthalten ist.  Darüber hinaus verfügt das QDK auch über Funktionen für Ressourcenschätzungen, die Erkenntnisse zur Leistung von Q#-Programmen liefern, die zu groß für die Ausführung mit dem Simulator sind.  Dies ist sehr nützlich für Algorithmusdesigner, weil sie ihre Programme für die Nutzung von weniger Ressourcen auslegen können (z. B. geringere Anzahl von Qubits für eine geringere Anzahl von Vorgängen), damit die Ausführung auf älterer Quantenhardware in kleinerem Umfang möglich ist.

### <a name="use-q-to-validate-hardware-performance"></a>Verwenden von Q# zum Überprüfen der Hardwareleistung

Der Vorteil von Q# besteht darin, dass ein einmal geschriebenes Programm zu Debugzwecken auf Quantensimulatoren und auf unterschiedlicher Quantencomputerhardware ausgeführt werden kann.  In Q# geschriebene Benchmarkprogramme können ausgeführt werden, um die Hardwareleistung zu überprüfen und die Ergebnisse zu vergleichen, während Quantencomputer weiterentwickelt bzw. neu entwickelt werden.  

## <a name="next-steps"></a>Nächste Schritte

* [Wo finde ich Informationen zu Quantencomputing?](xref:microsoft.quantum.overview.learn)
* [Einstieg in das Microsoft Quantum Development Kit](xref:microsoft.quantum.welcome)

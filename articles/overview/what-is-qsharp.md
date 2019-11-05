---
title: Was ist Q#?
description: Erfahren Sie mehr über Q#, eine von Microsoft geschaffene Programmiersprache zum Entwickeln von Anwendungen für Quantencomputer
author: natke
ms.author: nakersha
ms.date: 10/22/2019
ms.topic: article
uid: microsoft.quantum.overview.qsharp
ms.openlocfilehash: e04228ff62092a15c529297bd56b9ee48399f4a5
ms.sourcegitcommit: aa5e6f4a2deb4271a333d3f1b1eb69b5bb9a7bad
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2019
ms.locfileid: "73443952"
---
# <a name="what-is-q"></a>Was ist Q#?

Q# ist eine Programmiersprache mit Features, die sich speziell auf Quantencomputing beziehen. Q# bietet Quantenprogrammierern ein Framework, das es Ihnen erlaubt, sich auf die Algorithmen zu konzentrieren, ohne sich um technische Details wie die Optimierung von Gattersequenzen oder die physische Implementierung eines Quantencomputers kümmern zu müssen.

Die Programmiersprache Q# bietet Ihnen eine intuitive Menge von Typen, Operationen und logischen Ausdrücken zum Entwickeln von Algorithmen, ohne sich mit der internen Logik des Quantencomputers befassen zu müssen.

## <a name="code-algorithms"></a>Codealgorithmen

In den Anfängen des Quantencomputings wurden Algorithmen in Form von Diagrammen visualisiert, die den Schaltplänen aus dem klassischen Computing ähnelten.  Zwar hat sich das Schaltungsmodell über viele Jahre als sehr nützlich in der Forschung an Quantencomputing erwiesen, wir bei Microsoft glauben aber, dass Entwickler Quantenschaltungen hinter sich lassen und Quantenalgorithmen und -anwendungen mithilfe von Q# entwickeln können. Die Sprache Q# wurde entwickelt, um unsere Lehren aus jahrzehntelanger Erfahrung in der klassischen Softwareentwicklung zu nutzen und Quantenentwicklern die Funktionalität höherer Sprachen mit spezieller Ausrichtung auf Quantencomputing an die Hand zu geben.


## <a name="how-does-q-work"></a>Wie funktioniert Q#?

Einer der fundamentalen Bausteine von Q# ist der Typ `Qubit`, der nicht kopiert und auf den nicht direkt zugegriffen werden kann, ganz wie ein reales Qubit. Stattdessen können wir ihn messen und das Ergebnis der Messung in einer `Result`-Variable speichern, einem Q#-Typ, der zwei mögliche Werte annehmen kann: `Zero` und `One`. Konstrukte wie dieses stellen sicher, dass Algorithmen jederzeit die Gesetze der Quantenphysik beachten und auf Quantencomputern oder Simulatoren ordnungsgemäß ausgeführt werden können.

Q# schließt darüber hinaus Funktionen der klassischen Logik wie Bedingungen oder Schleifen mit einer Reihe von Feinheiten ein, um sicherzustellen, dass alle Quantenregeln beachtet werden. Beispielsweise müssen Quantenoperationen reversibel sein. Dies bringt einige Einschränkungen für die Ausführung von Schleifen mit sich.

Q#-Programme sind häufig mit einem in C# oder Python geschriebenen Hostprogramm gekoppelt, das eine komfortable Organisation von klassischem und Quantencode bieten kann. Über die Unterstützung von .NET-Sprachen wie C# und Python hinaus bietet das QDK mit dem IQ#-Jupyter-Kernel Unterstützung für Jupyter-Notebooks.

## <a name="use-q-to-learn-quantum-computing"></a>Verwenden von Q# zum Erlernen von Quantencomputing

Bisher mussten Sie zum Lernen von Quantencomputing das Schaltungsmodell lernen, um die Algorithmen in Form geordneter Sequenzen aus Quantengattern und Messungen zu verstehen. Mit Q# können Sie einen anderen Weg einschlagen: Lernen Sie Quantencomputing durch das Schreiben von Quantenprogrammen.

## <a name="use-q-to-design-quantum-algorithms"></a>Verwenden von Q# zum Entwerfen von Quantenalgorithmen

Q# verfügt über eine wachsende Zahl von Bibliotheken und benutzerdefinierten Typen, mit denen Sie Tools implementieren und erweiterte Quantenalgorithmen erstellen können. Sie müssen beispielsweise zwei Qubits q1 und q2 verschränken? Anstatt einzeln die erforderlichen Gatter anzuwenden, um die Qubits zu verschränken, können Sie die bereits integrierte Operation `PrepareEntangledState([q1], [q2])` verwenden.

## <a name="use-q-to-estimate-quantum-resources"></a>Verwenden von Q# zum Schätzen von Quantenressourcen

Sie können die Ausführung Ihres Q#-Programms simulieren, indem Sie den Quantensimulator für Zustände verwenden, der im Quantum Development Kit (QDK) enthalten ist.  Darüber hinaus verfügt das QDK auch über Funktionen für Ressourcenschätzungen, die Erkenntnisse zur Leistung von Q#-Programmen liefern, deren Größe eine Ausführung mit dem Simulator verhindert.  Dies ist sehr nützlich für Algorithmusdesigner, weil sie ihre Programme für die Nutzung von weniger Ressourcen auslegen können (z. B. geringere Anzahl von Qubits für eine geringere Anzahl von Vorgängen), damit die Ausführung auf älterer Quantenhardware in kleinerem Umfang möglich ist.   

## <a name="use-q-to-validate-hardware-performance"></a>Verwenden von Q# zum Überprüfen der Hardwareleistung

Der Vorteil von Q# besteht darin, dass ein einmal geschriebenes Programm zu Debugzwecken auf Quantensimulatoren und auf unterschiedlicher Quantencomputerhardware ausgeführt werden kann.  In Q# geschriebene Benchmarkprogramme können ausgeführt werden, um die Hardwareleistung zu überprüfen und die Ergebnisse zu vergleichen, während Quantencomputer weiterentwickelt bzw. neu entwickelt werden.  

## <a name="next-steps"></a>Nächste Schritte

* [Wie kann ich Quantencomputing lernen?](xref:microsoft.quantum.overview.learn)
* [Einstieg in das Microsoft Quantum Development Kit](xref:microsoft.quantum.welcome)

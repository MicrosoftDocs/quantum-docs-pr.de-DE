---
title: Was sind die Programmiersprache Q# und das QDK?
description: Hier finden Sie Informationen zum Microsoft Quantum Development Kit, zur Programmiersprache Q# und zur Erstellung von Quantenprogrammen.
author: bradben
ms.author: bradben
ms.date: 5/5/2020
ms.topic: overview
uid: microsoft.quantum.overview.q-sharp
ms.openlocfilehash: 55ac946aa935d3748b36ac99096a89d0db686835
ms.sourcegitcommit: a03d79ca3f0774161a9f86a15528d36e1291acce
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2020
ms.locfileid: "83433026"
---
# <a name="what-are-the-q-programming-language-and-qdk"></a>Was sind die Programmiersprache Q# und das QDK?

Q# ist die Open-Source-Programmiersprache von Microsoft zum Entwickeln und Ausführen von Quantenalgorithmen. Sie ist Teil des Quantum Development Kit (QDK), das [Q#-Bibliotheken](xref:microsoft.quantum.libraries), [Quantensimulatoren](xref:microsoft.quantum.machines), [Erweiterungen für andere Programmierumgebungen](xref:microsoft.quantum.install) sowie eine [API-Dokumentation](xref:microsoft.quantum.standardlibsintro) umfasst. Neben der Q#-Standardbibliothek enthält das QDK auch Bibliotheken für Chemie, maschinelles Lernen und numerische Werte.

Die Programmiersprache Q# nutzt vertraute Elemente aus Python, C# und F# und unterstützt ein einfaches Prozedurmodell zum Schreiben von Programmen mit Schleifen, If/Then-Anweisungen und gängigen Datentypen. Darüber hinaus führt sie aber auch neue quantenspezifische Datenstrukturen und Operationen ein.

## <a name="what-can-i-do-with-the-qdk"></a>Welche Möglichkeiten bietet das QDK?

Das QDK ist ein umfassendes Entwicklungskit für Q#, das mit gängigen Tools und Sprachen verwendet werden kann, um Quantenanwendungen zu entwickeln, die in verschiedenen Umgebungen ausführbar sind. Q#-Programme können als Befehlszeilen-App, über Jupyter Notebook-Instanzen oder mithilfe eines Python- oder .NET-Hostprogramms ausgeführt werden.

### <a name="develop-in-common-tools-and-environments"></a>Entwickeln in gängigen Tools und Umgebungen

Integrieren Sie Ihre Quantenentwicklung in [Visual Studio, Visual Studio Code](xref:microsoft.quantum.install.standalone) und [Jupyter Notebooks](xref:microsoft.quantum.install.jupyter). Nutzen Sie die integrierten APIs, um Ihre Programme mit [Python](xref:microsoft.quantum.install.python)- und [.NET](xref:microsoft.quantum.install.cs)-Hostsprachen zu kombinieren.

### <a name="try-quantum-operations-and-domain-specific-libraries"></a>Testen von Quantenoperationen und domänenspezifischen Bibliotheken

Schreiben und testen Sie Quantenalgorithmen, um sich mit Superposition, Verschränkung und anderen Quantenoperationen zu beschäftigen. Die Q#-Bibliotheken ermöglichen das Ausführen komplexer Quantenoperationen, ohne detaillierte Operationssequenzen entwickeln zu müssen.

### <a name="run-programs-in-simulators"></a>Ausführen von Programmen in Simulatoren

Führen Sie Ihre Quantenprogramme in einem Quantensimulator für den vollständigen Zustand oder in einem Toffoli-Simulator für einen eingeschränkten Bereich aus, oder testen Sie Ihren Q#-Code in verschiedenen Ressourcenschätzungen. 

## <a name="where-can-i-learn-more"></a>Wo kann ich mehr erfahren?

|||
| ---- | ---- |
| **Ich habe noch keine Erfahrung mit Quantencomputing.** | Unter [Grundlegendes zu Quantencomputing](xref:microsoft.quantum.overview.understanding) werden einige wichtige Konzepte der Quantenphysik und des Quantencomputings erläutert.|
| **Ich möchte mich intensiver mit der Programmiersprache Q# beschäftigen.** | Im [Q#-Benutzerhandbuch](xref:microsoft.quantum.guide) finden Sie Informationen zu Typen, Ausdrücken und Variablen sowie zur Struktur von Quantenprogrammen.|
| **Ich möchte einfach nur Quantenprogramme schreiben.** | Unter [Installieren des Microsoft Quantum Development Kit (QDK)](xref:microsoft.quantum.install) erfahren Sie, wie Sie Ihre Q#-Umgebung einrichten und mit dem Schreiben von Quantenprogrammen beginnen.|

## <a name="how-does-q-work"></a>Wie funktioniert Q#?

Ein Q#-Programm kann zu einer eigenständigen Befehlszeilenanwendung kompiliert oder durch ein in Python oder in einer .NET-Sprache geschriebenes Hostprogramm aufgerufen werden.

Wenn Sie das Programm kompilieren und ausführen, wird eine Instanz des Quantensimulators erstellt und der Q#-Code an ihn übergeben. Der Simulator verwendet den Q#-Code, um Qubits (Simulationen von Quantenteilchen) zu erstellen und Transformationen anzuwenden, um deren Zustand zu ändern. Danach werden die Ergebnisse der Quantenoperationen im Simulator an das Programm zurückgegeben.  

Durch die Isolierung des Q#-Codes im Simulator wird sichergestellt, dass die Algorithmen den Gesetzen der Quantenphysik folgen und ordnungsgemäß auf Quantencomputern ausgeführt werden können.

![qsharp-code-flow](~/media/qsharp-code-flow.png)

## <a name="how-do-i-use-the-qdk"></a>Wie wird das QDK verwendet?

Alles, was Sie zum Schreiben und Ausführen von Q#-Programmen benötigen, kann auf Ihrem lokalen Computer installiert und von dort aus ausgeführt werden – einschließlich des Q#-Compilers, der Q#-Bibliotheken und der Quantensimulatoren. Schlussendlich können Sie Ihre Q#-Programme remote auf einem echten Quantencomputer ausführen. Bis dahin liefern jedoch die über das QDK bereitgestellten Quantensimulatoren exakte und zuverlässige Ergebnisse.

- Das Ausführen von [Q# über die Befehlszeile](xref:microsoft.quantum.install.standalone) stellt die schnellste Einstiegsmöglichkeit dar.

- Führen Sie eigenständige [Jupyter Notebook-Instanzen mit IQ#](xref:microsoft.quantum.install.jupyter) aus – einer Jupyter-Erweiterung zum Kompilieren, Simulieren und Visualisieren von Q#-Programmen.

- Falls Sie damit vertraut sind, können Sie [Python](xref:microsoft.quantum.install.python) als Hostprogrammierplattform für Ihre ersten Schritte verwenden. Python wird nicht nur von Entwicklern, sondern auch von vielen Wissenschaftlern, Forschern und Lehrkräften genutzt.

- Wenn Sie bereits über Erfahrung mit [C#, F# oder VB.NET](xref:microsoft.quantum.install.cs) verfügen und mit der Visual Studio-Entwicklungsumgebung vertraut sind, können Sie Visual Studio durch Hinzufügen einiger weniger Erweiterungen für Q# bereit machen.  

## <a name="summary"></a>Zusammenfassung

Q# ist eine Open-Source-Programmiersprache zum Entwickeln von Quantenprogrammen. Sie enthält Bibliotheken, mit denen Sie komplexe Quantenoperationen erstellen können, sowie Quantensimulatoren, mit denen Sie Ihre Programme richtig ausführen und testen können. Q#-Programme können als eigenständige Apps ausgeführt oder über ein Python- oder .NET-Hostprogramm aufgerufen und auf Ihrem lokalen Computer geschrieben, ausgeführt und getestet werden.

## <a name="next-steps"></a>Nächste Schritte

> [!div class="nextstepaction"]
> [Lineare Algebra für Quantencomputing](xref:microsoft.quantum.overview.algebra)

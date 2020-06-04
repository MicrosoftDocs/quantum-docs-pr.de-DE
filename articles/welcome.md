---
uid: microsoft.quantum.welcome
title: Einstieg in das Quantum Development Kit (QDK)
description: Hier finden Sie Informationen zu den ersten Schritten mit dem Quantum Development Kit von Microsoft bei der Programmierung von Quantenprojekten in Q#.
author: natke
ms.author: nakersha
ms.date: 5/10/2020
ms.topic: overview
ms.openlocfilehash: 5fea46e43d9a3739e4b058781e1b52dff20b7e21
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "84327508"
---
# <a name="get-started-with-the-quantum-development-kit-qdk"></a>Einstieg in das Quantum Development Kit (QDK)

Willkommen beim Microsoft Quantum Development Kit!  

Das Quantum Development Kit (QDK) enthält alle Tools, die Sie für die Erstellung Ihrer eigenen Quantenprogramme und Experimente mit Q# benötigen. Q# ist eine Programmiersprache, die speziell für die Entwicklung von Quantenanwendungen konzipiert wurde.

Beginnen Sie mit dem [Leitfaden zur Installation des QDK](xref:microsoft.quantum.install), um sofort loszulegen.
Dort erfahren Sie Schritt für Schritt, wie Sie das Quantum Development Kit auf Windows-, Linux- oder macOS-Computern installieren, damit Sie Ihre eigenen Quantenprogramme schreiben können.

Sollten Sie noch keine Erfahrung mit Quantencomputing haben, finden Sie in der [Übersicht](xref:microsoft.quantum.overview.introduction) Informationen zu den Möglichkeiten von Quantencomputern sowie zu den Grundlagen des Quantencomputings.

## <a name="get-started-programming"></a>Einstieg in die Programmierung

Das Quantum Development Kit bietet viele Möglichkeiten, wie Sie die Entwicklung eines Quantenprogramms mit Q# erlernen können.
Unsere Tutorials helfen Ihnen beim schnellen Einstieg in die Welt des Quantencomputings:

* [Quanten-Zufallszahlengenerator](xref:microsoft.quantum.quickstarts.qrng): Beginnen Sie mit einer Q#-Anwendung im Hallo Welt-Stil, die eine kurze Einführung in die Konzepte des Quantencomputings bietet, während Sie in wenigen Minuten eine Quantenanwendung erstellen und ausführen.
* [Erkunden der Verschränkung mit Q#](xref:microsoft.quantum.write-program): Dieses Tutorial enthält Informationen zum Schreiben eines Q#-Programms zur Veranschaulichung einiger grundlegender Konzepte der Quantenprogrammierung.
    Wenn Sie noch nicht bereit sind, mit dem Programmieren zu beginnen, können Sie trotzdem fortfahren, ohne das QDK zu installieren, und sich einen Überblick über die Programmiersprache Q# und die ersten Konzepte des Quantencomputings verschaffen.
* [Grover-Suchalgorithmus](xref:microsoft.quantum.quickstarts.search): Ein Beispiel für ein Q#-Programm. Hiermit wird die hohe Leistungsfähigkeit von Q# in Bezug auf das Ausdrücken des Quantenalgorithmus mit dem Ziel verdeutlicht, untergeordnete Quantenoperationen zu abstrahieren.
    In diesem Tutorial erfahren Sie Schritt für Schritt, wie Sie das Programm unter Verwendung von Visual Studio oder Visual Studio Code als Q#-Befehlszeilenanwendung entwickeln.

### <a name="learning-further"></a>Weitere Informationen zum Lernen
* In den [Microsoft Learn-Modulen für Quantencomputing](https://docs.microsoft.com/learn/browse/?term=quantum) werden zentrale Konzepte vermittelt, mit denen Sie sich in Ihrer eigenen Geschwindigkeit und nach Ihrem eigenen Zeitplan vertraut machen können. Unser [erstes Modul](https://docs.microsoft.com/learn/modules/qsharp-create-first-quantum-development-kit/) enthält grundlegende Informationen zur Erstellung von Quantenprogrammen mit dem QDK.
* Informieren Sie sich über [Quanten-Katas](https://github.com/Microsoft/QuantumKatas), wenn Sie sich eingehender mit der Q#-Programmierung beschäftigen möchten. Hierbei handelt es sich um eine Sammlung mit Programmierübungen, die Sie im gewünschten Tempo durcharbeiten können und die als Einführung in das Quantencomputing mit Q# dienen.
    Viele dieser Katas sind auch als Q#-Notebooks verfügbar. 
* Unser [Repository mit Beispielen](https://github.com/Microsoft/Quantum) enthält mehrere Beispiele für das Schreiben von Quantenprogrammen mit Q#. Die meisten dieser Beispiele werden mit unseren Open-Source-[Quantenbibliotheken](https://github.com/Microsoft/QuantumLibraries) geschrieben, z. B. zu den Bereichen [Standard](xref:microsoft.quantum.libraries.standard.intro) und [Chemie](xref:microsoft.quantum.chemistry.concepts.intro) (weitere Informationen unten).

## <a name="key-concepts-for-quantum-computing"></a>Wichtige Konzepte für das Quantencomputing

Wenn die Quantenentwicklung neu für Sie ist, können wir gut nachvollziehen, dass dieses Thema ggf. etwas überwältigend erscheint. Diese wichtigen Konzepte erleichtern Ihnen den Einstieg in die Welt des Quantencomputings und verdeutlichen die Unterschiede zwischen Quantencomputing und klassischem Computing.

* [Grundlegendes zu Quantencomputing](xref:microsoft.quantum.overview.understanding)
* [Quantencomputer und -simulatoren](xref:microsoft.quantum.overview.simulators)
* [Was sind die Programmiersprache Q# und das QDK?](xref:microsoft.quantum.overview.q-sharp)
* [Lineare Algebra für Quantencomputing](xref:microsoft.quantum.overview.algebra)

## <a name="quantum-development-kit-documentation"></a>Dokumentation zum Quantum Development Kit

Die aktuelle Dokumentation enthält die folgenden zusätzlichen Themen.

### <a name="q-developer-guides"></a>Q#-Entwicklerhandbücher

* Im [Q#-Benutzerhandbuch](xref:microsoft.quantum.guide) werden die zentralen Konzepte im Zusammenhang mit der Erstellung von Quantenprogrammen in Q# erläutert.
* Unter [Quantensimulatoren und Hostanwendungen](xref:microsoft.quantum.machines) wird beschrieben, wie Quantenalgorithmen ausgeführt werden, welche Quantencomputer verfügbar sind und wie Sie für das Quantenprogramm einen Treiber schreiben, der nicht auf Q# basiert.

### <a name="q-libraries"></a>Q#-Bibliotheken

* Unter [Q#-Standardbibliotheken](xref:microsoft.quantum.libraries.standard.intro) werden die Vorgänge und Funktionen beschrieben, für die sowohl die Steuerung per klassischer Sprache als auch die Q#-Quantenalgorithmen unterstützt werden. 
    Zu den Themen gehören Ablaufsteuerung, Datenstrukturen, Fehlerkorrektur, Testen und Debuggen. 
* In der [Q#-Chemiebibliothek](xref:microsoft.quantum.chemistry.concepts.intro) werden die Vorgänge und Funktionen beschrieben, die eine Chemiesimulation im Bereich Quantencomputing unterstützen. Dies ist eine wichtige Anwendung des Quantencomputings. Zu den Themen gehören beispielsweise die Simulation der Hamilton-Dynamiken und die Quantenphasenschätzung.
* In der [Numerikbibliothek von Q#](xref:microsoft.quantum.numerics.intro) werden die Vorgänge und Funktionen beschrieben, die das Ausdrücken komplizierter arithmetischer Funktionen in Bezug auf die nativen Vorgänge von Zielcomputern unterstützen.
* Die [Q#-Bibliotheksreferenz](xref:microsoft.quantum.standardlibsintro) enthält Referenzinformationen zu Bibliotheksentitäten nach Namespace.

### <a name="general-quantum-computing"></a>Allgemeines Quantencomputing

* Der Artikel [Quantencomputingkonzepte](xref:microsoft.quantum.concepts.intro) enthält Themen, in denen die Bedeutung der linearen Algebra für das Quantencomputing, Art und Nutzung von Qubits, Lesen einer Quantenschaltung und mehr beschrieben wird.
* Das [Glossar zum Quantencomputing](xref:microsoft.quantum.glossary) enthält die wichtigen Begriffe des Quantencomputings und der Programmentwicklung.
    Wen dieses Thema neu für Sie ist, kann Ihnen das Glossar beim Durchlesen unserer Dokumentation als hilfreiche Referenz dienen.
* [Weitere Informationsquellen](xref:microsoft.quantum.more-information) enthält speziell ausgewählte Verweise auf umfassende Themen zum Quantencomputing.

### <a name="additional-info"></a>Zusätzliche Informationen

* [Versionshinweise für das Microsoft Quantum Development Kit](xref:microsoft.quantum.relnotes)


## <a name="be-a-part-of-the-q-open-source-community"></a>Beteiligen Sie sich an der Open-Source-Community zu Q#

Das Quantum Development Kit ist ein Open-Source-Development Kit, mit dem Entwickler das Quantencomputing für alle Benutzer besser zugänglich machen können, damit die drängendsten Probleme dieser Welt gelöst werden können.  Akademische Einrichtungen, die Open-Source-Software benötigen, können Q# bereitstellen, um das Erlernen und die Entwicklung mit Q# zu ermöglichen. Dank des Open-Source-Ansatzes des Development Kits haben Entwickler und Domänenexperten auch die Möglichkeit, Verbesserungen und Ideen per Code beizusteuern.

Ihr Feedback, Ihre Beteiligung und Ihre Beiträge zum Quantum Development Kit sind wichtig.  Informationen dazu, welche Quantum Development Kit-Quellen Sie nutzen können, wie Sie Feedback senden und wie Sie sich an den Entscheidungen beteiligen und einen Beitrag zu dieser stetig wachsenden Plattform zur Quantenentwicklung leisten können, finden Sie unter [Mitwirken am Quantum Development Kit](xref:microsoft.quantum.contributing).

Weitere allgemeine Informationen zur Quantencomputing-Initiative von Microsoft finden Sie unter [Microsoft Quantum](https://www.microsoft.com/en-us/quantum/).

---
uid: microsoft.quantum.welcome
title: Einstieg in das Quantum Development Kit (QDK)
description: Hier erfahren Sie, wie Sie mit Microsoft Quantum Development Kit (QDK) die ersten Schritte in der Programmierung von Quantenprojekten in Q# unternehmen.
author: natke
ms.author: nakersha
ms.date: 10/23/2019
ms.topic: overview
ms.openlocfilehash: cea39e47ec5e7e2ad97adbbb39ba586274564967
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907629"
---
# <a name="get-started-with-the-quantum-development-kit-qdk"></a>Einstieg in das Quantum Development Kit (QDK)

Willkommen beim Microsoft Quantum Development Kit!  
Das QDK enthält alle Tools, die Sie für die Erstellung Ihrer eigenen Quantenprogramme und Experimente mit Q# benötigen. Q# ist eine Programmiersprache, die speziell für die Entwicklung von Quantenanwendungen ausgelegt ist. 

Sie können den [Leitfaden zur Installation des QDK](xref:microsoft.quantum.install) verwenden, um sofort einzusteigen.
Anschließend wird Schritt für Schritt die Installation des Quantum Development Kit auf Windows-, Linux- bzw. macOS-Computern beschrieben, damit Sie Ihre eigenen Quantenprogramme schreiben können.

Falls Sie für den Einstieg in die Codeerstellung noch nicht bereit sind, aber mehr zum Quantencomputing und zu Q# erfahren möchten, ist das Lesen dieses Artikels trotzdem ratsam, um sich über die verfügbaren Ressourcen zu informieren. Der Abschnitt [Fünf Fragen zum Quantencomputing](#five-questions-about-quantum-computing) enthält Links zu den verschiedenen Bereichen, die für Sie interessant sind.

## <a name="get-started-programming"></a>Einstieg in die Programmierung

Das Quantum Development Kit bietet viele Möglichkeiten, wie Sie die Entwicklung eines Quantenprogramms mit Q# erlernen können.
Sie können unsere *Schnellstartanleitungen* nutzen, um die Leistungsstärke des Quantencomputings kennenzulernen:

* Der [Quanten-Zufallszahlengenerator](xref:microsoft.quantum.quickstarts.qrng) ist eine Q#-Anwendung im Stil „Hallo Welt“, die eine kurze Einführung in die Konzepte des Quantencomputings ermöglicht, während Sie in wenigen Minuten eine Quantenanwendung erstellen und ausführen.
* [Quantengrundlagen mit Q#](xref:microsoft.quantum.write-program) enthält Informationen zum Schreiben eines Q#-Programms, mit dem einige grundlegende Konzepte der Quantenprogrammierung beschrieben werden. 
    Wenn Sie noch nicht bereit sind, mit dem Programmieren zu beginnen, können Sie trotzdem fortfahren, ohne das QDK zu installieren, und sich einen Überblick über die Programmiersprache Q# und die ersten Konzepte des Quantencomputings verschaffen.
* [Grover-Suchalgorithmus](xref:microsoft.quantum.quickstarts.search) enthält ein Beispiel für ein Q#-Programm. Hiermit wird die hohe Leistungsfähigkeit von Q# in Bezug auf das Ausdrücken des Quantenalgorithmus mit dem Ziel verdeutlicht, Quantenvorgänge auf niedriger Ebene zu abstrahieren. 
    Diese Schnellstartanleitung enthält eine Beschreibung der Entwicklung des Programms basierend auf einer Vielzahl von Programmierumgebungen (mit einem Python-Host oder einem Host in der .NET-Sprache und mit Visual Studio oder Visual Studio Code).

### <a name="learning-further"></a>Weitere Informationen zum Lernen
* Informieren Sie sich über [Quanten-Katas](https://github.com/Microsoft/QuantumKatas), wenn Sie sich eingehender mit der Q#-Programmierung beschäftigen möchten. Hierbei handelt es sich um eine Sammlung mit Programmierübungen, die Sie im gewünschten Tempo durcharbeiten können und die als Einführung in das Quantencomputing mit Q# dienen.
    Viele dieser Katas sind auch als Q#-Notebooks verfügbar. 
* Unser [Repository mit Beispielen](https://github.com/Microsoft/Quantum) enthält mehrere Beispiele für das Schreiben von Quantenprogrammen mit Q#. Die meisten dieser Beispiele werden mit unseren Open-Source-[Quantenbibliotheken](https://github.com/Microsoft/QuantumLibraries) geschrieben, z. B. zu den Bereichen [Standard](xref:microsoft.quantum.libraries.standard.intro) und [Chemie](xref:microsoft.quantum.chemistry.concepts.intro) (weitere Informationen unten).

## <a name="five-questions-about-quantum-computing"></a>Fünf Fragen zum Quantencomputing

Wenn die Quantenentwicklung neu für Sie ist, können wir gut nachvollziehen, dass dieses Thema ggf. etwas überwältigend erscheint. Daher haben wir Ressourcen bereitgestellt, die Ihnen den Einstieg in das Erlernen des Quantencomputings erleichtern sollen. Wir sind uns sicher, dass Sie nach dem Durcharbeiten dieser kurzen Artikel schon bald mit der Programmierung beginnen möchten.
* [Was ist Quantencomputing?](xref:microsoft.quantum.overview.what)
* [Was können Quantencomputer?](xref:microsoft.quantum.overview.computers)
* [Warum sollte ich das Quantencomputing erlernen?](xref:microsoft.quantum.overview.why)
* [Was ist Q#?](xref:microsoft.quantum.overview.qsharp)
* [Wie erlerne ich das Quantencomputing mit Q#?](xref:microsoft.quantum.overview.learn)

## <a name="quantum-development-kit-documentation"></a>Dokumentation zum Quantum Development Kit

Die aktuelle Dokumentation enthält die folgenden zusätzlichen Themen.

### <a name="using-q"></a>Verwenden von Q#
* Unter [Verfahren der Quantenentwicklung](xref:microsoft.quantum.techniques.intro) sind die wichtigen Konzepte der Erstellung von Quantenprogrammen in Q# angegeben. Zu den beschriebenen Themenbereichen gehören Dateistrukturen, Vorgänge und Funktionen, die Verwendung von Qubits und einige Themen für Fortgeschrittene.
* In der [Referenz zur Sprache Q#](xref:microsoft.quantum.language.intro) finden Sie Details zur Sprache Q#, z. B. Typmodell, Ausdrücke, Anweisungen und Compilerverwendung.
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

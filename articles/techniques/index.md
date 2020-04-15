---
title: Verfahren der Quantenentwicklung
description: Enthält grundlegende Informationen zur Entwicklung von Q#-Programmen, und es wird beschrieben, wie Sie Vorgänge, Funktionen, Variablen und Qubits verwenden und ein einfaches Quantenprogramm erstellen.
keywords: Vermeiden Sie es, Schlüsselwörter hinzuzufügen oder zu bearbeiten, ohne Ihren SEO-Experten zurate zu ziehen.
author: QuantumWriter
ms.author: MSFT-alias-person-or-DL
ms.date: 9/20/2019
ms.topic: article-type-from-white-list
uid: microsoft.quantum.techniques.intro
ms.openlocfilehash: e5b7fbde18afbc0333d89f70c5e4596848e30f4f
ms.sourcegitcommit: 9d1c045cf1a2c3e19030cb38dbc7496dbd24ab58
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2020
ms.locfileid: "77907714"
---
# <a name="quantum-development-techniques"></a>Verfahren der Quantenentwicklung

In diesem Abschnitt der Dokumentation werden die grundlegenden Konzepte beschrieben, die zum Erstellen von Quantenprogrammen in Q# und zum Interagieren mit diesen Programmen aus klassischen Anwendungen verwendet werden.
Wir setzen ein *gewisses Maß* an Wissen im Bereich Quantencomputing voraus (z. B. wie unter [Quantencomputingkonzepte](xref:microsoft.quantum.concepts.intro) beschrieben), aber Sie können von diesen Abschnitten auch profitieren, wenn Sie kein Experte sind.

Die Abschnitte enthalten die folgenden Informationen.

- [Q#-Programmübersicht](xref:microsoft.quantum.techniques.file-structure) enthält eine Übersicht über den Zweck und die Funktionalität der Programmiersprache Q#. 
    Es wird verdeutlicht, dass Q# *keine* Sprache ist, um nur die Quantenmechanik zu simulieren, obwohl diese Funktionalität von unserem Simulator für den vollständig ausgelasteten Zustand natürlich bereitgestellt wird. 
    Stattdessen wurde Q# mit Blick auf die Zukunft konzipiert, und die zugehörigen Programme beschreiben, wie ein klassischer Steuerungscomputer mit Qubits *interagiert*. 

- Unter [Vorgänge und Funktionen](xref:microsoft.quantum.techniques.opsandfunctions) werden die beiden aufrufbaren Elemente von Q# beschrieben: *Vorgänge*, für die Aktionen mit Qubits und Quantensystemen durchgeführt werden, und *Funktionen*, für die ausschließlich klassische Informationen genutzt werden. 
    Quantencomputing wäre nicht möglich, ohne dass klassische Informationen und Quanteninformationen zusammenarbeiten. 
    In diesem Abschnitt wird beschrieben, wie Sie diese aufrufbaren Elemente in der Ablaufsteuerung eines Q#-Programms definieren und nutzen.

- Unter [Lokale Variablen](xref:microsoft.quantum.techniques.local-variables) wird die Rolle von Variablen in Q#-Programmen sowie deren effektive Nutzung beschrieben. 
    Es wird vor allem der Unterschied zwischen unveränderlichen und veränderlichen Variablen und deren Zuweisung bzw. erneute Zuweisung beschrieben.

- Unter [Arbeiten mit Qubits](xref:microsoft.quantum.techniques.qubits) erhalten Sie Informationen zu den Features von Q#, die Sie verwenden können, um einzelne Qubits und Qubit-Systeme zu nutzen. 
    Hierbei geht es um deren Zuordnung, die Durchführung von entsprechenden Vorgängen und schließlich deren Messung. 
    Darüber hinaus werden einige nützliche Verfahren der Ablaufsteuerung beschrieben.

- Unter [Zusammenfügen des Gesamtbilds](xref:microsoft.quantum.techniques.puttingittogether) nutzen Sie die Verfahren aus den obigen Abschnitten zum Erstellen eines Programms, mit dem eine **Quantenteleportation** durchgeführt wird. Hierbei werden zwei klassische Bits genutzt, um für den vollständigen Zustand eines Qubits die Teleportation auf ein anderes Qubit durchzuführen.

- Unter [Weitere Informationen](xref:microsoft.quantum.techniques.going-further) werden erweiterte Verfahren vorgestellt, die hilfreich sein können, wenn Sie sich mit der komplexeren Quantenprogrammierung beschäftigen möchten. 
    Es werden die Nutzung von Vorgängen mit *Typparametrisierung* und Funktionen in Q# beschrieben, die eine Ablaufsteuerung höherer Ordnung ermöglichen, indem sie gegenüber den spezifischen Typen der Ein- bzw. Ausgabe agnostisch bleiben. Außerdem erhalten Sie Informationen zum *Ausleihen* von Qubits. 
    Letzteres unterscheidet sich von der grundlegenden Qubit-Zuordnung darin, dass für einen Q#-Vorgang „Dirty Qubits“ (ohne zwingende Initialisierung für einen bekannten Zustand) verwendet werden können, um Computingvorgänge zu unterstützen.

- Unter [Testen und Debuggen](xref:microsoft.quantum.techniques.testing-and-debugging) werden einige Verfahren beschrieben, mit denen sichergestellt werden kann, dass sich Ihr Code wie gewünscht verhält. 
    Aufgrund der allgemeinen Opazität von Quanteninformationen sind zum Debuggen eines Quantenprogramms ggf. spezielle Verfahren erforderlich. 
    Glücklicherweise unterstützt Q# nicht nur quantenspezifische, sondern auch viele klassische Debugverfahren, mit denen Programmierer bereits vertraut sind. Beispiele hierfür sind das Erstellen bzw. Ausführen von Komponententests in Q#, Einbetten von *Assertionen* in Werten und Wahrscheinlichkeiten in Ihrem Code und die `Dump`-Funktionen, mit denen der Zustand des Zielcomputers ausgegeben wird. 
    Letzteres kann zusammen mit unserem Simulator für den vollständig ausgelasteten Zustand genutzt werden, um bestimmte Teile von Berechnungen zu debuggen, indem einige Einschränkungen für Quantenvorgänge umgangen werden (z. B. das Theorem zum Thema „Kein Klonen“).


![Quantencomputing](~/media/mobius_strip_preview.png)

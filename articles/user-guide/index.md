---
title: Q#-Benutzerhandbuch
description: Übersicht über Zweck und Inhalt des Benutzerhandbuchs
author: gillenhaalb
ms.author: a-gibec
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide
no-loc:
- Q#
- $$v
ms.openlocfilehash: 979e468cc743bd9125eaba0b71f794977c914447
ms.sourcegitcommit: b930bb59a1ba8f41d2edc9ed98197109aa8c7f1b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96231756"
---
# <a name="the-no-locq-user-guide"></a>Q#-Benutzerhandbuch

Willkommen beim Q#-Benutzerhandbuch. 

In den verschiedenen Themen dieses Handbuchs werden einige Grundlagen für die Entwicklung von Quantum-Programmen mithilfe von Q# vorgestellt.

Im [Q#-Sprachführer ](xref:microsoft.quantum.qsharp.index) finden Sie eine vollständige Spezifikation und Dokumentation der Quantum-Programmiersprache Q#. 

## <a name="user-guide-contents"></a>Inhalt des Benutzerhandbuchs

- [Q#-Programme](xref:microsoft.quantum.guide.programs): Eine kurze Einführung in Quantum-Programme in Q# 

- [Möglichkeiten zum Ausführen eines Q#-Programms:](xref:microsoft.quantum.guide.host-programs) Beschreibt, wie ein Q#-Programm ausgeführt wird, und bietet eine Übersicht über die verschiedenen Möglichkeiten, wie Sie das Programm aufrufen können: über die Befehlszeile, in Q#-Jupyter Notebook-Instanzen oder über ein klassisches Hostprogramm, das in Python oder in einer .NET-Sprache geschrieben ist.

- [Testen und Debuggen:](xref:microsoft.quantum.guide.testingdebugging) Hier werden einige Verfahren beschrieben, mit denen sichergestellt werden kann, dass sich Ihr Code wie gewünscht verhält. 
    Aufgrund der allgemeinen Opazität von Quanteninformationen sind zum Debuggen eines Quantenprogramms ggf. spezielle Verfahren erforderlich. 
    Erfreulicherweise unterstützt Q# nicht nur quantenspezifische, sondern auch viele klassische Debugverfahren, mit denen Programmierer bereits vertraut sind. Beispiele hierfür sind das Erstellen und Ausführen von Komponententests in Q#, Einbetten von *Assertionen* in Werten und Wahrscheinlichkeiten in Ihrem Code und die `Dump`-Funktionen, mit denen der Zustand der Zielcomputer ausgegeben wird. 
    Letzteres kann zusammen mit unserem Simulator für den vollständigen Zustand genutzt werden, um bestimmte Teile von Berechnungen zu debuggen, indem einige Einschränkungen für Quantenvorgänge umgangen werden (z. B. das [Theorem zum Thema „Kein Klonen“](xref:microsoft.quantum.concepts.pauli)).

### <a name="quantum-simulators-and-resource-estimators"></a>Quantensimulatoren und Ressourcenschätzungen

- [Quantensimulatoren und Hostanwendungen:](xref:microsoft.quantum.machines) Eine Übersicht über die verschiedenen verfügbaren Simulatoren sowie Informationen zur Zusammenarbeit von Hostprogrammen und Zielcomputern zur Ausführung von Q#-Programmen

- [Simulator für den vollständigen Zustand:](xref:microsoft.quantum.machines.full-state-simulator) Der Zielcomputer zum Simulieren des vollständigen Quantenzustands. Hilfreich zum vollständigen Ausführen oder Debuggen kleinerer Programme (weniger als ein paar Dutzend Qubits).

- [Zielcomputer für die Ressourcenschätzung:](xref:microsoft.quantum.machines.resources-estimator) Dient zum Schätzen der erforderlichen Ressourcen für das Ausführen einer bestimmten Instanz eines Q#-Vorgangs auf einem Quantencomputer.

- [Ablaufverfolgungssimulator für Quantencomputer:](xref:microsoft.quantum.machines.qc-trace-simulator.intro) Dient zum Ausführen eines Quantenprogramms, ohne tatsächlich den Zustand eines Quantencomputers zu simulieren, und eignet sich daher zum Ausführen von Quantenprogrammen mit Tausenden von Qubits. Hilfreich zum Debuggen von klassischem Code in einem Quantenprogramm sowie zum Schätzen der benötigten Ressourcen.

- [Quantum Development Kit-Toffoli-Simulator:](xref:microsoft.quantum.machines.toffoli-simulator) Ein spezieller Quantensimulator, der mit Millionen von Qubits verwendet werden kann – allerdings nur für Programme mit einem eingeschränkten Satz von Quantenvorgängen (X, CNOT und mehrfach gesteuertes X).

### <a name="quick-reference-pages"></a>Kurzübersichten

- [IQ#-Magic-Befehle:](xref:microsoft.quantum.guide.quickref.iqsharp) Kurzübersicht über IQ#-Magic-Befehle in Q#-Jupyter Notebook-Instanzen.

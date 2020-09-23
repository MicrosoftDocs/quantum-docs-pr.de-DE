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
ms.openlocfilehash: f0680e773c8233d6c4f1acb742b3cc38dbc069d5
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/21/2020
ms.locfileid: "90834753"
---
# <a name="the-no-locq-user-guide"></a>Q#-Benutzerhandbuch

Willkommen beim Q#-Benutzerhandbuch. 

In den verschiedenen Themen dieses Handbuchs finden Sie eine Beschreibung der grundlegenden Konzepte der Sprache Q# sowie alle Informationen, die Sie zum Schreiben von Quantenprogrammen benötigen.

## <a name="user-guide-contents"></a>Inhalt des Benutzerhandbuchs

- [Q#-Grundlagen:](xref:microsoft.quantum.guide.basics) Ein erster Überblick über den Zweck und die Funktionen der Programmiersprache Q#. 

- [Möglichkeiten zum Ausführen eines Q#-Programms:](xref:microsoft.quantum.guide.host-programs) Beschreibt, wie ein Q#-Programm ausgeführt wird, und bietet eine Übersicht über die verschiedenen Möglichkeiten, wie Sie das Programm aufrufen können: über die Befehlszeile, in Q#-Jupyter Notebook-Instanzen oder über ein klassisches Hostprogramm, das in Python oder in einer .NET-Sprache geschrieben ist.

### <a name="no-locq-language"></a>Sprache Q#

- [Typen in Q#:](xref:microsoft.quantum.guide.types) Hier finden Sie Informationen zum Typmodell von Q# sowie zur Syntax für die Angabe und Verwendung von Typen.

- [Typausdrücke in Q#:](xref:microsoft.quantum.guide.expressions) Hier erfahren Sie, wie Sie Werte für die einzelnen Typen in Q# angeben, auf sie verweisen, sie kombinieren und mit ihnen arbeiten können. 

### <a name="using-no-locq"></a>Verwenden von Q#

- [Q#-Dateistruktur:](xref:microsoft.quantum.guide.filestructure) Hier werden Struktur und Syntax einer Q#-Datei (`*.qs`) beschrieben.

- [Vorgänge und Funktionen in Q#:](xref:microsoft.quantum.guide.operationsfunctions) Hier werden die beiden aufrufbaren Typen der Sprache Q# beschrieben: *Vorgänge* (einschließlich Aktionen für Qubit-Register) und *Funktionen* (nur für klassische Informationen verwendbar). 
    Hier erfahren Sie, wie Sie sie definieren und aufrufen – einschließlich Adjoint- und Controlled-Versionen von Quantenvorgängen.

- [Variablen:](xref:microsoft.quantum.guide.variables) In diesem Thema werden die Rolle von Variablen in Q#-Programmen sowie deren effektive Nutzung beschrieben. 
    Dort finden Sie beispielsweise Informationen zu Bindungsbereichen, zum Unterschied zwischen unveränderlichen und veränderlichen Variablen sowie zu deren Zuweisung bzw. erneuter Zuweisung.

- [Arbeiten mit Qubits:](xref:microsoft.quantum.guide.qubits) Hier werden die Features von Q# beschrieben, die Sie für die Nutzung einzelner Qubits und Qubit-Systeme verwenden können, insbesondere für ihre Zuordnung, die Durchführung von Vorgängen und ihre Messung. 

- [Ablaufsteuerung in Q#:](xref:microsoft.quantum.guide.controlflow) Hier wird die Programmierung von in Q# verfügbaren Ablaufsteuerungsmustern beschrieben. Dazu zählt neben zahlreichen Standardverfahren (etwa bedingte Verarbeitung, *for*-Schleifen, *while-Schleifen*) auch das quantenspezifische Muster der Wiederholung bis zum Erfolg (*repeat-until-success*).

- [Testen und Debuggen:](xref:microsoft.quantum.guide.testingdebugging) Hier werden einige Verfahren beschrieben, mit denen sichergestellt werden kann, dass sich Ihr Code wie gewünscht verhält. 
    Aufgrund der allgemeinen Opazität von Quanteninformationen sind zum Debuggen eines Quantenprogramms ggf. spezielle Verfahren erforderlich. 
    Erfreulicherweise unterstützt Q# nicht nur quantenspezifische, sondern auch viele klassische Debugverfahren, mit denen Programmierer bereits vertraut sind. Beispiele hierfür sind das Erstellen und Ausführen von Komponententests in Q#, Einbetten von *Assertionen* in Werten und Wahrscheinlichkeiten in Ihrem Code und die `Dump`-Funktionen, mit denen der Zustand der Zielcomputer ausgegeben wird. 
    Letzteres kann zusammen mit unserem Simulator für den vollständigen Zustand genutzt werden, um bestimmte Teile von Berechnungen zu debuggen, indem einige Einschränkungen für Quantenvorgänge umgangen werden (z. B. das [Theorem zum Thema „Kein Klonen“](xref:microsoft.quantum.concepts.pauli)).

### <a name="quantum-simulators-and-resource-estimators"></a>Quantensimulatoren und Ressourcenschätzungen

- [Quantensimulatoren und Hostanwendungen:](xref:microsoft.quantum.machines) Eine Übersicht über die verschiedenen verfügbaren Simulatoren sowie Informationen zum allgemeinen Ausführungsmodell zwischen Hostprogramm und den Zielcomputern.

- [Simulator für den vollständigen Zustand:](xref:microsoft.quantum.machines.full-state-simulator) Der Zielcomputer zum Simulieren des vollständigen Quantenzustands. Hilfreich zum vollständigen Ausführen oder Debuggen kleinerer Programme (weniger als ein paar Dutzend Qubits).

- [Zielcomputer für die Ressourcenschätzung:](xref:microsoft.quantum.machines.resources-estimator) Dient zum Schätzen der erforderlichen Ressourcen für das Ausführen einer bestimmten Instanz eines Q#-Vorgangs auf einem Quantencomputer.

- [Ablaufverfolgungssimulator für Quantencomputer:](xref:microsoft.quantum.machines.qc-trace-simulator.intro) Dient zum Ausführen eines Quantenprogramms, ohne tatsächlich den Zustand eines Quantencomputers zu simulieren, und eignet sich daher zum Ausführen von Quantenprogrammen mit Tausenden von Qubits. Hilfreich zum Debuggen von klassischem Code in einem Quantenprogramm sowie zum Schätzen der benötigten Ressourcen.

- [Quantum Development Kit-Toffoli-Simulator:](xref:microsoft.quantum.machines.toffoli-simulator) Ein spezieller Quantensimulator, der mit Millionen von Qubits verwendet werden kann – allerdings nur für Programme mit einem eingeschränkten Satz von Quantenvorgängen (X, CNOT und mehrfach gesteuertes X).

### <a name="quick-reference-pages"></a>Kurzübersichten

- [IQ#-Magic-Befehle:](xref:microsoft.quantum.guide.quickref.iqsharp) Kurzübersicht über IQ#-Magic-Befehle in Q#-Jupyter Notebook-Instanzen.

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
# <a name="the-no-locq-user-guide"></a><span data-ttu-id="49878-103">Q#-Benutzerhandbuch</span><span class="sxs-lookup"><span data-stu-id="49878-103">The Q# User Guide</span></span>

<span data-ttu-id="49878-104">Willkommen beim Q#-Benutzerhandbuch.</span><span class="sxs-lookup"><span data-stu-id="49878-104">Welcome to the Q# User Guide!</span></span> 

<span data-ttu-id="49878-105">In den verschiedenen Themen dieses Handbuchs werden einige Grundlagen für die Entwicklung von Quantum-Programmen mithilfe von Q# vorgestellt.</span><span class="sxs-lookup"><span data-stu-id="49878-105">In the different topics of this guide, we introduce some of the basics for developing quantum programs using Q#.</span></span>

<span data-ttu-id="49878-106">Im [Q#-Sprachführer ](xref:microsoft.quantum.qsharp.index) finden Sie eine vollständige Spezifikation und Dokumentation der Quantum-Programmiersprache Q#.</span><span class="sxs-lookup"><span data-stu-id="49878-106">We refer to the [Q# language guide](xref:microsoft.quantum.qsharp.index) for a full specification and documentation of the Q# quantum programming language.</span></span> 

## <a name="user-guide-contents"></a><span data-ttu-id="49878-107">Inhalt des Benutzerhandbuchs</span><span class="sxs-lookup"><span data-stu-id="49878-107">User Guide Contents</span></span>

- <span data-ttu-id="49878-108">[Q#-Programme](xref:microsoft.quantum.guide.programs): Eine kurze Einführung in Quantum-Programme in Q#</span><span class="sxs-lookup"><span data-stu-id="49878-108">[Q# programs](xref:microsoft.quantum.guide.programs): An quick introduction to quantum programs in Q#.</span></span> 

- <span data-ttu-id="49878-109">[Möglichkeiten zum Ausführen eines Q#-Programms:](xref:microsoft.quantum.guide.host-programs) Beschreibt, wie ein Q#-Programm ausgeführt wird, und bietet eine Übersicht über die verschiedenen Möglichkeiten, wie Sie das Programm aufrufen können: über die Befehlszeile, in Q#-Jupyter Notebook-Instanzen oder über ein klassisches Hostprogramm, das in Python oder in einer .NET-Sprache geschrieben ist.</span><span class="sxs-lookup"><span data-stu-id="49878-109">[Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs): describes how a Q# program is run, and provides an overview of the various ways you can call the program: from the command line, in Q# Jupyter Notebooks, or from a classical host program written in Python or a .NET language.</span></span>

- <span data-ttu-id="49878-110">[Testen und Debuggen:](xref:microsoft.quantum.guide.testingdebugging) Hier werden einige Verfahren beschrieben, mit denen sichergestellt werden kann, dass sich Ihr Code wie gewünscht verhält.</span><span class="sxs-lookup"><span data-stu-id="49878-110">[Testing and debugging](xref:microsoft.quantum.guide.testingdebugging): Details some techniques for making sure your code is doing what it is supposed to do.</span></span> 
    <span data-ttu-id="49878-111">Aufgrund der allgemeinen Opazität von Quanteninformationen sind zum Debuggen eines Quantenprogramms ggf. spezielle Verfahren erforderlich.</span><span class="sxs-lookup"><span data-stu-id="49878-111">Due to the general opacity of quantum information, debugging a quantum program can require specialized techniques.</span></span> 
    <span data-ttu-id="49878-112">Erfreulicherweise unterstützt Q# nicht nur quantenspezifische, sondern auch viele klassische Debugverfahren, mit denen Programmierer bereits vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="49878-112">Fortunately, Q# supports many of the classical debugging techniques programmers are familiar with, as well as those that are quantum-specific.</span></span> <span data-ttu-id="49878-113">Beispiele hierfür sind das Erstellen und Ausführen von Komponententests in Q#, Einbetten von *Assertionen* in Werten und Wahrscheinlichkeiten in Ihrem Code und die `Dump`-Funktionen, mit denen der Zustand der Zielcomputer ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="49878-113">These include creating and running unit tests in Q#, embedding *assertions* on values and probabilities in your code, and the `Dump` functions which output the states of target machines.</span></span> 
    <span data-ttu-id="49878-114">Letzteres kann zusammen mit unserem Simulator für den vollständigen Zustand genutzt werden, um bestimmte Teile von Berechnungen zu debuggen, indem einige Einschränkungen für Quantenvorgänge umgangen werden (z. B. das [Theorem zum Thema „Kein Klonen“](xref:microsoft.quantum.concepts.pauli)).</span><span class="sxs-lookup"><span data-stu-id="49878-114">The latter can be used alongside our full-state simulator to debug certain parts of computations by skirting some quantum limitations, for example, the [no-cloning theorem](xref:microsoft.quantum.concepts.pauli).</span></span>

### <a name="quantum-simulators-and-resource-estimators"></a><span data-ttu-id="49878-115">Quantensimulatoren und Ressourcenschätzungen</span><span class="sxs-lookup"><span data-stu-id="49878-115">Quantum Simulators and Resource Estimators</span></span>

- <span data-ttu-id="49878-116">[Quantensimulatoren und Hostanwendungen:](xref:microsoft.quantum.machines) Eine Übersicht über die verschiedenen verfügbaren Simulatoren sowie Informationen zur Zusammenarbeit von Hostprogrammen und Zielcomputern zur Ausführung von Q#-Programmen</span><span class="sxs-lookup"><span data-stu-id="49878-116">[Quantum simulators and host applications](xref:microsoft.quantum.machines): An overview of the different simulators available, as well of how host programs and target machines work together to run Q# programs.</span></span>

- <span data-ttu-id="49878-117">[Simulator für den vollständigen Zustand:](xref:microsoft.quantum.machines.full-state-simulator) Der Zielcomputer zum Simulieren des vollständigen Quantenzustands.</span><span class="sxs-lookup"><span data-stu-id="49878-117">[Full state simulator](xref:microsoft.quantum.machines.full-state-simulator): The target machine which simulates the full quantum state.</span></span> <span data-ttu-id="49878-118">Hilfreich zum vollständigen Ausführen oder Debuggen kleinerer Programme (weniger als ein paar Dutzend Qubits).</span><span class="sxs-lookup"><span data-stu-id="49878-118">Useful for fully running or debugging smaller-scale programs (less than a few dozen qubits)</span></span>

- <span data-ttu-id="49878-119">[Zielcomputer für die Ressourcenschätzung:](xref:microsoft.quantum.machines.resources-estimator) Dient zum Schätzen der erforderlichen Ressourcen für das Ausführen einer bestimmten Instanz eines Q#-Vorgangs auf einem Quantencomputer.</span><span class="sxs-lookup"><span data-stu-id="49878-119">[Resources estimator](xref:microsoft.quantum.machines.resources-estimator): Estimates the resources required to run a given instance of a Q# operation on a quantum computer.</span></span>

- <span data-ttu-id="49878-120">[Ablaufverfolgungssimulator für Quantencomputer:](xref:microsoft.quantum.machines.qc-trace-simulator.intro) Dient zum Ausführen eines Quantenprogramms, ohne tatsächlich den Zustand eines Quantencomputers zu simulieren, und eignet sich daher zum Ausführen von Quantenprogrammen mit Tausenden von Qubits.</span><span class="sxs-lookup"><span data-stu-id="49878-120">[Trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro): Runs a quantum program without actually simulating the state of a quantum computer, and therefore can run quantum programs that use thousands of qubits.</span></span> <span data-ttu-id="49878-121">Hilfreich zum Debuggen von klassischem Code in einem Quantenprogramm sowie zum Schätzen der benötigten Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="49878-121">Useful for debugging classical code within a quantum program, as well as estimating resources required.</span></span>

- <span data-ttu-id="49878-122">[Quantum Development Kit-Toffoli-Simulator:](xref:microsoft.quantum.machines.toffoli-simulator) Ein spezieller Quantensimulator, der mit Millionen von Qubits verwendet werden kann – allerdings nur für Programme mit einem eingeschränkten Satz von Quantenvorgängen (X, CNOT und mehrfach gesteuertes X).</span><span class="sxs-lookup"><span data-stu-id="49878-122">[Toffoli simulator](xref:microsoft.quantum.machines.toffoli-simulator): A special-purpose quantum simulator that can be used with millions of qubits, but only for programs with a restricted set of quantum operations - X, CNOT, and multi-controlled X.</span></span>

### <a name="quick-reference-pages"></a><span data-ttu-id="49878-123">Kurzübersichten</span><span class="sxs-lookup"><span data-stu-id="49878-123">Quick Reference Pages</span></span>

- <span data-ttu-id="49878-124">[IQ#-Magic-Befehle:](xref:microsoft.quantum.guide.quickref.iqsharp) Kurzübersicht über IQ#-Magic-Befehle in Q#-Jupyter Notebook-Instanzen.</span><span class="sxs-lookup"><span data-stu-id="49878-124">[IQ# Magic Commands](xref:microsoft.quantum.guide.quickref.iqsharp): Quick reference page for IQ# magic commands within Q# Jupyter Notebooks.</span></span>

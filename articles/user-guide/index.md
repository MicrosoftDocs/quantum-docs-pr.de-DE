---
title: Q#-Benutzerhandbuch
description: Übersicht über Zweck und Inhalt des Benutzerhandbuchs
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide
ms.openlocfilehash: f535aaedbe6ce181375d48f7023409ad8212c702
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2020
ms.locfileid: "83430610"
---
# <a name="the-q-user-guide"></a><span data-ttu-id="6dd2c-103">Q#-Benutzerhandbuch</span><span class="sxs-lookup"><span data-stu-id="6dd2c-103">The Q# User Guide</span></span>

<span data-ttu-id="6dd2c-104">Willkommen beim Q#-Benutzerhandbuch!</span><span class="sxs-lookup"><span data-stu-id="6dd2c-104">Welcome to the Q# User Guide!</span></span> 

<span data-ttu-id="6dd2c-105">Hier finden Sie eine Beschreibung der grundlegenden Konzepte der Sprache Q# sowie alle Informationen, die Sie zum Schreiben von Quantenprogrammen benötigen.</span><span class="sxs-lookup"><span data-stu-id="6dd2c-105">Here we detail the core concepts of the Q# language and all the information you need to write quantum programs.</span></span>

## <a name="user-guide-contents"></a><span data-ttu-id="6dd2c-106">Inhalt des Benutzerhandbuchs</span><span class="sxs-lookup"><span data-stu-id="6dd2c-106">User Guide Contents</span></span>

- <span data-ttu-id="6dd2c-107">[Q#-Grundlagen:](xref:microsoft.quantum.guide.basics) Ein erster Überblick über den Zweck und die Funktionen der Programmiersprache Q#.</span><span class="sxs-lookup"><span data-stu-id="6dd2c-107">[Q# Basics](xref:microsoft.quantum.guide.basics): an introductory overview of the purpose and functionality of the Q# programming language.</span></span> 

### <a name="q-language"></a><span data-ttu-id="6dd2c-108">Q#-Sprache</span><span class="sxs-lookup"><span data-stu-id="6dd2c-108">Q# Language</span></span>

- <span data-ttu-id="6dd2c-109">[Typen in Q#:](xref:microsoft.quantum.guide.types) Hier finden Sie Informationen zum Typmodell von Q# sowie zur Syntax für die Angabe und Verwendung von Typen.</span><span class="sxs-lookup"><span data-stu-id="6dd2c-109">[Types in Q#](xref:microsoft.quantum.guide.types): lays out the Q# type model and describes the syntax for specifying and working with types.</span></span>

- <span data-ttu-id="6dd2c-110">[Typausdrücke:](xref:microsoft.quantum.guide.expressions) Hier erfahren Sie, wie Sie Werte für die einzelnen Typen in Q# angeben, auf sie verweisen, sie kombinieren und mit ihnen arbeiten.</span><span class="sxs-lookup"><span data-stu-id="6dd2c-110">[Type Expressions](xref:microsoft.quantum.guide.expressions): details how to specify, reference, combine, and operate on values of each type in Q#.</span></span> 

### <a name="using-q"></a><span data-ttu-id="6dd2c-111">Verwenden von Q#</span><span class="sxs-lookup"><span data-stu-id="6dd2c-111">Using Q#</span></span>

- <span data-ttu-id="6dd2c-112">[Q#-Dateistruktur:](xref:microsoft.quantum.guide.filestructure) Hier werden Struktur und Syntax einer Q#-Datei (`*.qs`) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6dd2c-112">[Q# File Structure](xref:microsoft.quantum.guide.filestructure): describes the structure and syntax of a `*.qs` Q# file.</span></span>

- <span data-ttu-id="6dd2c-113">Unter [Vorgänge und Funktionen in Q#](xref:microsoft.quantum.guide.operationsfunctions) werden die beiden aufrufbaren Typen der Sprache Q# beschrieben. Dabei handelt es sich um *Vorgänge* (einschließlich Aktionen für Qubit-Register) und um *Funktionen* (nur für klassische Informationen verwendbar).</span><span class="sxs-lookup"><span data-stu-id="6dd2c-113">[Operations and Functions](xref:microsoft.quantum.guide.operationsfunctions): details the two callable types of the Q# language: *operations*, which include action on qubit registers and *functions*, which strictly work with classical information.</span></span> 
    <span data-ttu-id="6dd2c-114">Hier erfahren Sie, wie Sie sie definieren und aufrufen – einschließlich Adjoint- und Controlled-Versionen von Quantenvorgängen.</span><span class="sxs-lookup"><span data-stu-id="6dd2c-114">Here you see how to define and call them, including the adjoint and controlled versions of quantum operations.</span></span>

- <span data-ttu-id="6dd2c-115">Unter [Variablen](xref:microsoft.quantum.guide.variables) werden die Rolle von Variablen in Q#-Programmen sowie deren effektive Nutzung beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6dd2c-115">[Variables](xref:microsoft.quantum.guide.variables): describes the role of variables within Q# programs and how to leverage them effectively.</span></span> 
    <span data-ttu-id="6dd2c-116">Dort finden Sie beispielsweise Informationen zu Bindungsbereichen, zum Unterschied zwischen unveränderlichen und veränderlichen Variablen sowie zu deren Zuweisung bzw. erneuter Zuweisung.</span><span class="sxs-lookup"><span data-stu-id="6dd2c-116">For example, you can find information about binding scopes, as well as the difference between immutable/mutable variables and how to assign/re-assign them.</span></span>

- <span data-ttu-id="6dd2c-117">Unter [Arbeiten mit Qubits](xref:microsoft.quantum.guide.qubits) erhalten Sie Informationen zu den Features von Q#, die Sie verwenden können, um einzelne Qubits und Qubit-Systeme zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="6dd2c-117">[Working with qubits](xref:microsoft.quantum.guide.qubits): describes the features of Q# used to address individual qubits and systems of qubits.</span></span> 
    <span data-ttu-id="6dd2c-118">Hierbei geht es um deren Zuordnung, die Durchführung von entsprechenden Vorgängen und schließlich deren Messung.</span><span class="sxs-lookup"><span data-stu-id="6dd2c-118">Specifically, that entails their allocation, performing operations on them, and ultimately their measurement.</span></span> 

- <span data-ttu-id="6dd2c-119">[Ablaufsteuerung:](xref:microsoft.quantum.guide.controlflow) Hier wird die Programmierung von in Q# verfügbaren Ablaufsteuerungsmustern beschrieben. Dazu zählt neben zahlreichen Standardverfahren (bedingte Ausführung, for-Schleifen, while-Schleifen usw.) auch das quantenspezifische Muster der Wiederholung bis zum Erfolg (repeat-until-success).</span><span class="sxs-lookup"><span data-stu-id="6dd2c-119">[Control Flow](xref:microsoft.quantum.guide.controlflow): details the programming control flow patterns available in Q#, which includes many standard techniques (conditional execution, for loops, while loops, etc.) as well as the quantum-specific "Repeat-Until-Success" pattern.</span></span>

- <span data-ttu-id="6dd2c-120">[Testen und Debuggen:](xref:microsoft.quantum.guide.testingdebugging) Hier werden einige Verfahren beschrieben, mit denen sichergestellt werden kann, dass sich Ihr Code wie gewünscht verhält.</span><span class="sxs-lookup"><span data-stu-id="6dd2c-120">[Testing and debugging](xref:microsoft.quantum.guide.testingdebugging): details some techniques for making sure your code is doing what it is supposed to do.</span></span> 
    <span data-ttu-id="6dd2c-121">Aufgrund der allgemeinen Opazität von Quanteninformationen sind zum Debuggen eines Quantenprogramms ggf. spezielle Verfahren erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6dd2c-121">Due to the general opacity of quantum information, debugging a quantum program can require specialized techniques.</span></span> 
    <span data-ttu-id="6dd2c-122">Glücklicherweise unterstützt Q# nicht nur quantenspezifische, sondern auch viele klassische Debugverfahren, mit denen Programmierer bereits vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="6dd2c-122">Fortunately, Q# supports many of the classical debugging techniques programmers are used to, as well as those that are quantum-specific.</span></span> <span data-ttu-id="6dd2c-123">Beispiele hierfür sind das Erstellen bzw. Ausführen von Komponententests in Q#, Einbetten von *Assertionen* in Werten und Wahrscheinlichkeiten in Ihrem Code und die `Dump`-Funktionen, mit denen der Zustand des Zielcomputers ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6dd2c-123">These include creating/running unit tests in Q#, embedding *assertions* on values and probabilities in your code, and the `Dump` functions which output the state of target machine.</span></span> 
    <span data-ttu-id="6dd2c-124">Letzteres kann zusammen mit unserem Simulator für den vollständigen Zustand genutzt werden, um bestimmte Teile von Berechnungen zu debuggen, indem einige Einschränkungen für Quantenvorgänge umgangen werden (z. B. das Theorem zum Thema „Kein Klonen“).</span><span class="sxs-lookup"><span data-stu-id="6dd2c-124">The latter can be used alongside our full-state simulator to debug certain parts of computations by skirting some quantum limitations (e.g. the no-cloning theorem).</span></span>

### <a name="quantum-simulators-and-resource-estimators"></a><span data-ttu-id="6dd2c-125">Quantensimulatoren und Ressourcenschätzungen</span><span class="sxs-lookup"><span data-stu-id="6dd2c-125">Quantum Simulators and Resource Estimators</span></span>

- <span data-ttu-id="6dd2c-126">[Quantensimulatoren und Hostanwendungen:](xref:microsoft.quantum.machines) Eine Übersicht über die verschiedenen verfügbaren Simulatoren sowie Informationen zum allgemeinen Ausführungsmodell zwischen Hostprogramm und den Zielcomputern.</span><span class="sxs-lookup"><span data-stu-id="6dd2c-126">[Quantum simulators and host applications](xref:microsoft.quantum.machines): an overview of the different simulators available, as well as the general execution model between host program and target machines.</span></span>

- <span data-ttu-id="6dd2c-127">[Simulator für den vollständigen Zustand:](xref:microsoft.quantum.machines.full-state-simulator) Der Zielcomputer zum Simulieren des vollständigen Quantenzustands.</span><span class="sxs-lookup"><span data-stu-id="6dd2c-127">[Full state simulator](xref:microsoft.quantum.machines.full-state-simulator): the target machine which simulates the full quantum state.</span></span> <span data-ttu-id="6dd2c-128">Hilfreich zum vollständigen Ausführen oder Debuggen kleinerer Programme (weniger als ein paar Dutzend Qubits).</span><span class="sxs-lookup"><span data-stu-id="6dd2c-128">Useful for fully executing or debugging smaller scale programs (less than a couple dozen qubits)</span></span>

- <span data-ttu-id="6dd2c-129">[Ressourcenschätzung:](xref:microsoft.quantum.machines.resources-estimator) Dient zum Schätzen der erforderlichen Ressourcen für das Ausführen einer bestimmten Instanz eines Q#-Vorgangs auf einem Quantencomputer.</span><span class="sxs-lookup"><span data-stu-id="6dd2c-129">[Resources estimator](xref:microsoft.quantum.machines.resources-estimator): estimates the resources required to run a given instance of a Q# operation on a quantum computer.</span></span>

- <span data-ttu-id="6dd2c-130">[Ablaufverfolgungssimulator:](xref:microsoft.quantum.machines.qc-trace-simulator.intro) Dient zum Ausführen eines Quantenprogramms, ohne tatsächlich den Zustand eines Quantencomputers zu simulieren, und eignet sich daher zum Ausführen von Quantenprogrammen mit Tausenden von Qubits.</span><span class="sxs-lookup"><span data-stu-id="6dd2c-130">[Trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro): executes a quantum program without actually simulating the state of a quantum computer, and therefore can execute quantum programs that use thousands of qubits.</span></span> <span data-ttu-id="6dd2c-131">Hilfreich zum Debuggen von klassischem Code in einem Quantenprogramm sowie zum Schätzen der benötigten Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="6dd2c-131">Useful for debugging classical code within a quantum program, as well as estimating resources required.</span></span>

- <span data-ttu-id="6dd2c-132">[Toffoli-Simulator:](xref:microsoft.quantum.machines.toffoli-simulator) Ein spezieller Quantensimulator, der mit Millionen von Qubits verwendet werden kann – allerdings nur für Programme mit einem eingeschränkten Satz von Quantenvorgängen (X, CNOT und mehrfach gesteuertes X).</span><span class="sxs-lookup"><span data-stu-id="6dd2c-132">[Toffoli simulator](xref:microsoft.quantum.machines.toffoli-simulator): a special purpose quantum simulator that can be used with millions of qubits, but only for programs with a restricted set of quantum operations (namely X, CNOT, and multi-controlled X).</span></span>

### <a name="quick-reference-pages"></a><span data-ttu-id="6dd2c-133">Kurzübersichten</span><span class="sxs-lookup"><span data-stu-id="6dd2c-133">Quick Reference Pages</span></span>

- <span data-ttu-id="6dd2c-134">[IQ#-Magic-Befehle:](xref:microsoft.quantum.guide.quickref.iqsharp) Kurzübersicht über IQ#-Magic-Befehle in Q#-Jupyter Notebook-Instanzen.</span><span class="sxs-lookup"><span data-stu-id="6dd2c-134">[IQ# Magic Commands](xref:microsoft.quantum.guide.quickref.iqsharp): Quick reference page for IQ# magic commands within Q# Jupyter Notebooks.</span></span>

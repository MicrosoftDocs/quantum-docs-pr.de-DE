---
title: Abrufen von Ressourcen Zählungen | Microsoft-Dokumentation
description: Abrufen von Ressourcen Anzahlen docs
author: guanghaolow
ms.author: gulow
ms.date: 10/23/2018
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.examples.resourcecounts
ms.openlocfilehash: f9311c1987ced4336c4e98bdb984fbee009e9acc
ms.sourcegitcommit: aa5e6f4a2deb4271a333d3f1b1eb69b5bb9a7bad
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2019
ms.locfileid: "73442466"
---
# <a name="obtaining-resource-counts"></a><span data-ttu-id="0fcd8-103">Abrufen der Ressourcenanzahl</span><span class="sxs-lookup"><span data-stu-id="0fcd8-103">Obtaining resource counts</span></span>

<span data-ttu-id="0fcd8-104">Die Kosten für das Simulieren von $n $ Qubits auf klassischen Computern werden exponentiell mit $n $ skaliert.</span><span class="sxs-lookup"><span data-stu-id="0fcd8-104">The cost of simulating $n$ qubits on classical computers scales exponentially with $n$.</span></span> <span data-ttu-id="0fcd8-105">Dadurch wird die Größe einer Quantum-Chemie-Simulation, die wir mit dem vollständigen Simulator ausführen können, erheblich eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="0fcd8-105">This greatly limits the size of a quantum chemistry simulation we may perform with the full-state simulator.</span></span> <span data-ttu-id="0fcd8-106">Für große Instanzen von Chemie können wir dennoch nützliche Informationen erhalten.</span><span class="sxs-lookup"><span data-stu-id="0fcd8-106">For large instances of chemistry, we may nevertheless obtain useful information.</span></span> <span data-ttu-id="0fcd8-107">Hier wird erläutert, wie Ressourcenkosten, wie z. b. die Anzahl der T-Gates oder CNOT Gates, zum Simulieren der Chemie mithilfe des [Trace Simulators](xref:microsoft.quantum.machines.qc-trace-simulator.intro)automatisiert abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="0fcd8-107">Here, we examine how resource costs, such as the number of T-gates or CNOT gates, for simulating chemistry may be obtained in an automated fashion using the [trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span> <span data-ttu-id="0fcd8-108">Diese Informationen informieren uns darüber, wann Quantum-Computer groß genug sein könnten, um diese Quantum-Chemie-Algorithmen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="0fcd8-108">Such information informs us of when quantum computers might be large enough to run these quantum chemistry algorithms.</span></span> <span data-ttu-id="0fcd8-109">Weitere Informationen finden Sie im `GetGateCount` Beispiel.</span><span class="sxs-lookup"><span data-stu-id="0fcd8-109">For reference, see the provided `GetGateCount` sample.</span></span>

<span data-ttu-id="0fcd8-110">Nehmen wir an, dass wir bereits über eine `FermionHamiltonian` Instanz verfügen, z. b. aus dem broombridge-Schema geladen, wie im Beispiel zum [Laden von Dateien](xref:microsoft.quantum.chemistry.examples.loadhamiltonian) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0fcd8-110">Let us assume that we already have a `FermionHamiltonian` instance, say, loaded from the Broombridge schema as discussed in the [loading-from-file](xref:microsoft.quantum.chemistry.examples.loadhamiltonian) example.</span></span> 

```csharp
    // Filename of Hamiltonian to be loaded.
    var filename = "...";

    // This deserializes Broombridge.
    var problem = Broombridge.Deserializers.DeserializeBroombridge(filename).ProblemDescriptions.First();

    // This is a data structure representing the Jordan-Wigner encoding 
    // of the Hamiltonian that we may pass to a Q# algorithm.
    var qSharpData = problem.ToQSharpFormat();
```

<span data-ttu-id="0fcd8-111">Die Syntax zum Abrufen von Ressourcenschätzungen ist nahezu identisch mit der Ausführung des Algorithmus im vollständigen Simulator.</span><span class="sxs-lookup"><span data-stu-id="0fcd8-111">The syntax for obtaining resource estimates is almost identical to running the algorithm on the full-state simulator.</span></span> <span data-ttu-id="0fcd8-112">Wir wählen einfach einen anderen Zielcomputer aus.</span><span class="sxs-lookup"><span data-stu-id="0fcd8-112">We simply choose a different target machine.</span></span> <span data-ttu-id="0fcd8-113">Im Hinblick auf Ressourcenschätzungen genügt es, die Kosten eines einzelnen trockschritts oder eines durch das qubisierungsverfahren erstellten Quantum Walk auszuwerten.</span><span class="sxs-lookup"><span data-stu-id="0fcd8-113">For the purposes of resource estimates, it suffices to evaluate the cost of a single Trotter step, or a quantum walk created by the Qubitization technique.</span></span> <span data-ttu-id="0fcd8-114">Die Bausteine zum Aufrufen dieser Algorithmen lauten wie folgt.</span><span class="sxs-lookup"><span data-stu-id="0fcd8-114">The boilerplate for invoking these algorithms is as follows.</span></span>

```qsharp
//////////////////////////////////////////////////////////////////////////
// Using Trotterization //////////////////////////////////////////////////
//////////////////////////////////////////////////////////////////////////

/// # Summary
/// This allocates qubits and applies a single Trotter step.
operation RunTrotterStep (qSharpData: JordanWignerEncodingData) : Unit {
    
    // The data describing the Hamiltonian for all these steps is contained in
    // `qSharpData`
    // We use a Product formula, also known as `Trotterization` to
    // simulate the Hamiltonian.
    // The integrator step size does not affect the gate cost of a single step.
    let trotterStepSize = 1.0;
    
    // Order of integrator
    let trotterOrder = 1;
    let (nQubits, (rescaleFactor, oracle)) = TrotterStepOracle(qSharpData, trotterStepSize, trotterOrder);
    
    // We not allocate qubits an run a single step.
    using (qubits = Qubit[nQubits]) {
        oracle(qubits);
        ResetAll(qubits);
    }
}


//////////////////////////////////////////////////////////////////////////
// Using Qubitization ////////////////////////////////////////////////////
//////////////////////////////////////////////////////////////////////////

/// # Summary
/// This allocates qubits and applies a single qubitization step.
operation RunQubitizationStep (qSharpData: JordanWignerEncodingData) : Double {
    
    // The data describing the Hamiltonian for all these steps is contained in
    // `qSharpData`
    let (nQubits, (l1Norm, oracle)) = QubitizationOracle(qSharpData);
    
    // We now allocate qubits and run a single step.
    using (qubits = Qubit[nQubits]) {
        oracle(qubits);
        ResetAll(qubits);
    }
    
    return l1Norm;
}
```

<span data-ttu-id="0fcd8-115">Nun konfigurieren wir den Ablauf Verfolgungs Simulator, um die für uns interessanten Ressourcen nachzuverfolgen.</span><span class="sxs-lookup"><span data-stu-id="0fcd8-115">We now configure the trace simulator to track the resources we are interested in.</span></span> <span data-ttu-id="0fcd8-116">In diesem Fall zählen wir primitive Quantum-Vorgänge, indem wir das `usePrimitiveOperationsCounter`-Flag auf `true`festlegen.</span><span class="sxs-lookup"><span data-stu-id="0fcd8-116">In this case, we count primitive quantum operations by setting the `usePrimitiveOperationsCounter` flag to `true`.</span></span> <span data-ttu-id="0fcd8-117">Ein technischer Detail `throwOnUnconstraintMeasurement` ist auf `false` festgelegt, um Ausnahmen in Fällen zu vermeiden, in denen der Q #-Code die Wahrscheinlichkeit von Messergebnissen nicht ordnungsgemäß bestätigt, wenn eine solche ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0fcd8-117">A technical detail `throwOnUnconstraintMeasurement` is set to `false` to avoid exceptions in cases where the Q# code does not correctly assert of probability of measurement outcomes, if any are performed.</span></span>

```csharp
private static QCTraceSimulator CreateAndConfigureTraceSim()
{
    // Create and configure Trace Simulator
    var config = new QCTraceSimulatorConfiguration()
    {
        usePrimitiveOperationsCounter = true,
        throwOnUnconstraintMeasurement = false
    };

    return new QCTraceSimulator(config);
}
```

<span data-ttu-id="0fcd8-118">Nun führen wir den Quantum-Algorithmus wie folgt aus dem Treiber Programm aus.</span><span class="sxs-lookup"><span data-stu-id="0fcd8-118">We now run the quantum algorithm from the driver program as follows.</span></span>

```csharp
// Instantiate a trace simulator instance
QCTraceSimulator sim = CreateAndConfigureTraceSim();

// Run the quantum algorithm on the trace simulator.
RunQubitizationStep.Run(sim, qSharpData);

// Print all resource counts to file.
var gateStats = sim.ToCSV();
foreach (var x in gateStats)
{
    System.IO.File.WriteAllLines($"QubitizationGateCountEstimates.{x.Key}.csv", new string[] { x.Value });
}
```
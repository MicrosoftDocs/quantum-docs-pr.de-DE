---
title: Abrufen der Ressourcenanzahl
description: Erfahren Sie, wie Sie Ressourcenschätzungen mithilfe eines Quantum-Ablauf Verfolgungs Simulators abrufen.
author: guanghaolow
ms.author: gulow
ms.date: 10/23/2018
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.examples.resourcecounts
no-loc:
- Q#
- $$v
ms.openlocfilehash: 35c16e622a390b730ad7385efcc365c212e981fe
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2020
ms.locfileid: "87869323"
---
# <a name="obtaining-resource-counts"></a>Abrufen der Ressourcenanzahl

Die Kosten für das Simulieren von $n $ Qubits auf klassischen Computern werden exponentiell mit $n $ skaliert. Dadurch wird die Größe einer Quantum-Chemie-Simulation, die wir mit dem vollständigen Simulator ausführen können, erheblich eingeschränkt. Für große Instanzen von Chemie können wir dennoch nützliche Informationen erhalten. Hier wird erläutert, wie Ressourcenkosten, wie z. b. die Anzahl der T-Gates oder CNOT Gates, zum Simulieren der Chemie mithilfe des [Trace Simulators](xref:microsoft.quantum.machines.qc-trace-simulator.intro)automatisiert abgerufen werden können. Diese Informationen informieren uns darüber, wann Quantum-Computer groß genug sein könnten, um diese Quantum-Chemie-Algorithmen auszuführen. Weitere Informationen finden Sie im bereitgestellten `GetGateCount` Beispiel.

Wir gehen davon aus, dass wir bereits über eine- `FermionHamiltonian` Instanz verfügen, z. b. aus dem broombridge-Schema geladen, wie im Beispiel zum [Laden von Dateien](xref:microsoft.quantum.chemistry.examples.loadhamiltonian) beschrieben. 

```csharp
    // Filename of Hamiltonian to be loaded.
    var filename = "...";

    // This deserializes Broombridge.
    var problem = Broombridge.Deserializers.DeserializeBroombridge(filename).ProblemDescriptions.First();

    // This is a data structure representing the Jordan-Wigner encoding 
    // of the Hamiltonian that we may pass to a Q# algorithm.
    var qSharpData = problem.ToQSharpFormat();
```

Die Syntax zum Abrufen von Ressourcenschätzungen ist nahezu identisch mit der Ausführung des Algorithmus im vollständigen Simulator. Wir wählen einfach einen anderen Zielcomputer aus. Im Hinblick auf Ressourcenschätzungen genügt es, die Kosten eines einzelnen trockschritts oder eines durch das qubisierungsverfahren erstellten Quantum Walk auszuwerten. Die Bausteine zum Aufrufen dieser Algorithmen lauten wie folgt.

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

Nun konfigurieren wir den Ablauf Verfolgungs Simulator, um die für uns interessanten Ressourcen nachzuverfolgen. In diesem Fall zählen die primitiven Quantum-Vorgänge, indem das-Flag auf festgelegt wird `usePrimitiveOperationsCounter` `true` . Ein technisches Detail `throwOnUnconstraintMeasurement` ist auf festgelegt, `false` um Ausnahmen in Fällen zu vermeiden, in denen der Q# Code die Wahrscheinlichkeit von Messergebnissen nicht ordnungsgemäß bestätigt, wenn eine solche ausgeführt wird.

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

Nun führen wir den Quantum-Algorithmus wie folgt aus dem Treiber Programm aus.

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
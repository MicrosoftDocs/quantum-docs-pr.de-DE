---
title: Tiefen Counter | Ablauf Verfolgungs Simulator für Quantum-Computer | Microsoft-Dokumentation
description: Übersicht über den Ablauf Verfolgungs Simulator für Quantum-Computer
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.depth-counter
ms.openlocfilehash: f5fcaa64e91290d377eeba597df2e307e187277c
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/29/2019
ms.locfileid: "73184898"
---
# <a name="depth-counter"></a><span data-ttu-id="5443d-103">Tiefen Counter</span><span class="sxs-lookup"><span data-stu-id="5443d-103">Depth Counter</span></span>

<span data-ttu-id="5443d-104">Der `Depth Counter` ist Teil des Ablauf [Verfolgungs Simulators](xref:microsoft.quantum.machines.qc-trace-simulator.intro)für Quantum-Computer.</span><span class="sxs-lookup"><span data-stu-id="5443d-104">The `Depth Counter` is a part of the quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span>
<span data-ttu-id="5443d-105">Es wird verwendet, um die Anzahl der tiefen jedes in einem Quantum-Programm aufgerufenen Vorgangs zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="5443d-105">It is used to gather counts of the depth of every operation invoked in a quantum program.</span></span> <span data-ttu-id="5443d-106">Alle Vorgänge aus <xref:microsoft.quantum.intrinsic> werden in Form einzelner Qubit-Drehungen, t Gates, einzelner Qubit Clifford Gates, CNOT Gates und Messungen von Multi-Qubit Pauli Observables ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="5443d-106">All operations from <xref:microsoft.quantum.intrinsic> are expressed in terms of single qubit rotations, T gates, single qubit Clifford gates, CNOT gates and measurements of multi-qubit Pauli observables.</span></span> <span data-ttu-id="5443d-107">Benutzer können die Tiefe für die einzelnen primitiven Vorgänge über das `gateTimes`-Feld <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration>festlegen.</span><span class="sxs-lookup"><span data-stu-id="5443d-107">Users can set the depth for each of the primitive operations via the `gateTimes` field of <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration>.</span></span>

<span data-ttu-id="5443d-108">Standardmäßig haben alle Vorgänge eine Tiefe von 0, außer dem T-Gate, das Tiefe 1 hat.</span><span class="sxs-lookup"><span data-stu-id="5443d-108">By default, all operations have depth 0 except the T gate which has depth 1.</span></span> <span data-ttu-id="5443d-109">Dies bedeutet, dass standardmäßig nur die T-Tiefe der Vorgänge berechnet wird (was häufig wünschenswert ist).</span><span class="sxs-lookup"><span data-stu-id="5443d-109">This means that by default, only the T depth of operations is computed (which is often desirable).</span></span> <span data-ttu-id="5443d-110">Gesammelte Statistiken werden über alle Ränder des Vorgangs Aufruf Diagramms aggregiert.</span><span class="sxs-lookup"><span data-stu-id="5443d-110">Collected statistics are aggregated over all the edges of the operations call graph.</span></span> 

<span data-ttu-id="5443d-111">Wir berechnen nun die <xref:microsoft.quantum.intrinsic.t> Tiefe des <xref:microsoft.quantum.intrinsic.ccnot> Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="5443d-111">Let us now compute the <xref:microsoft.quantum.intrinsic.t> depth of the <xref:microsoft.quantum.intrinsic.ccnot> operation.</span></span> <span data-ttu-id="5443d-112">Wir verwenden den folgenden Q #-Treibercode:</span><span class="sxs-lookup"><span data-stu-id="5443d-112">We will use the following Q# driver code:</span></span> 

```qsharp
open Microsoft.Quantum.Primitive;
operation CCNOTDriver() : Unit {

    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    }
}
```

## <a name="using-depth-counter-within-a-c-program"></a><span data-ttu-id="5443d-113">Verwenden des tiefen Zählers C# innerhalb eines Programms</span><span class="sxs-lookup"><span data-stu-id="5443d-113">Using Depth Counter within a C# Program</span></span>

<span data-ttu-id="5443d-114">Um zu überprüfen, ob `CCNOT` `T` Tiefe 5 hat und `CCNOTDriver` `T` Tiefe 6 hat, können C# wir den folgenden Code verwenden:</span><span class="sxs-lookup"><span data-stu-id="5443d-114">To check that `CCNOT` has `T` depth 5 and `CCNOTDriver` has `T` depth 6 we can use the following C# code:</span></span>

```csharp 
using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;
using System.Diagnostics;
var config = new QCTraceSimulatorConfiguration();
config.useDepthCounter = true;
var sim = new QCTraceSimulator(config);
var res = CCNOTDriver.Run(sim).Result;

double tDepth = sim.GetMetric<Primitive.CCNOT, CCNOTDriver>(DepthCounter.Metrics.Depth);
double tDepthAll = sim.GetMetric<CCNOTDriver>(DepthCounter.Metrics.Depth);
```

<span data-ttu-id="5443d-115">Der erste Teil des Programms führt `CCNOTDriver`aus.</span><span class="sxs-lookup"><span data-stu-id="5443d-115">The first part of the program executes `CCNOTDriver`.</span></span> <span data-ttu-id="5443d-116">Im zweiten Teil verwenden wir die-Methode `QCTraceSimulator.GetMetric`, um die `T` Tiefe von `CCNOT` und `CCNOTDriver`zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="5443d-116">In the second part, we use the method `QCTraceSimulator.GetMetric` to get the `T` depth of `CCNOT` and `CCNOTDriver`:</span></span> 

```csharp
double tDepth = sim.GetMetric<Primitive.CCNOT, CCNOTDriver>(DepthCounter.Metrics.Depth);
double tDepthAll = sim.GetMetric<CCNOTDriver>(DepthCounter.Metrics.Depth);
```

<span data-ttu-id="5443d-117">Zum Schluss können Sie zum Ausgeben aller Statistiken, die von `Depth Counter` im CSV-Format gesammelt werden, Folgendes verwenden:</span><span class="sxs-lookup"><span data-stu-id="5443d-117">Finally, to output all the statistics collected by `Depth Counter` in CSV format we can use the following:</span></span>
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.depthCounter];
```

## <a name="see-also"></a><span data-ttu-id="5443d-118">Informationen finden Sie auch unter</span><span class="sxs-lookup"><span data-stu-id="5443d-118">See also</span></span> ##

- <span data-ttu-id="5443d-119">Übersicht über den Ablauf [Verfolgungs Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) für Quantum-Computer</span><span class="sxs-lookup"><span data-stu-id="5443d-119">The quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>

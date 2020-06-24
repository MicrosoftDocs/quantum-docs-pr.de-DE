---
title: Tiefen Counter
description: Erfahren Sie mehr über den Microsoft QDK-tiefen Zähler, der die Anzahl der tiefen jedes in einem Quantum-Programm aufgerufenen Vorgangs sammelt.
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.depth-counter
ms.openlocfilehash: d532a9f512b8c87d83d62ed26e3bb67e1b6f668b
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274936"
---
# <a name="depth-counter"></a><span data-ttu-id="4b439-103">Tiefen Counter</span><span class="sxs-lookup"><span data-stu-id="4b439-103">Depth Counter</span></span>

<span data-ttu-id="4b439-104">Der `Depth Counter` ist ein Teil des Ablauf [Verfolgungs Simulators](xref:microsoft.quantum.machines.qc-trace-simulator.intro)für Quantum-Computer.</span><span class="sxs-lookup"><span data-stu-id="4b439-104">The `Depth Counter` is a part of the quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span>
<span data-ttu-id="4b439-105">Es wird verwendet, um die Anzahl der tiefen jedes in einem Quantum-Programm aufgerufenen Vorgangs zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="4b439-105">It is used to gather counts of the depth of every operation invoked in a quantum program.</span></span> <span data-ttu-id="4b439-106">Alle Vorgänge von <xref:microsoft.quantum.intrinsic> werden als einzelne Qubit-Drehungen, T Gates, Single Qubit Clifford Gates, CNOT Gates und Messungen von Multi-Qubit Pauli Observables ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="4b439-106">All operations from <xref:microsoft.quantum.intrinsic> are expressed in terms of single qubit rotations, T gates, single qubit Clifford gates, CNOT gates and measurements of multi-qubit Pauli observables.</span></span> <span data-ttu-id="4b439-107">Benutzer können die Tiefe für jeden der primitiven Vorgänge über das- `gateTimes` Feld von festlegen <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> .</span><span class="sxs-lookup"><span data-stu-id="4b439-107">Users can set the depth for each of the primitive operations via the `gateTimes` field of <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration>.</span></span>

<span data-ttu-id="4b439-108">Standardmäßig haben alle Vorgänge eine Tiefe von 0, außer dem T-Gate, das Tiefe 1 hat.</span><span class="sxs-lookup"><span data-stu-id="4b439-108">By default, all operations have depth 0 except the T gate which has depth 1.</span></span> <span data-ttu-id="4b439-109">Dies bedeutet, dass standardmäßig nur die T-Tiefe der Vorgänge berechnet wird (was häufig wünschenswert ist).</span><span class="sxs-lookup"><span data-stu-id="4b439-109">This means that by default, only the T depth of operations is computed (which is often desirable).</span></span> <span data-ttu-id="4b439-110">Gesammelte Statistiken werden über alle Ränder des Vorgangs Aufruf Diagramms aggregiert.</span><span class="sxs-lookup"><span data-stu-id="4b439-110">Collected statistics are aggregated over all the edges of the operations call graph.</span></span> 

<span data-ttu-id="4b439-111">Wir berechnen nun die <xref:microsoft.quantum.intrinsic.t> Tiefe des <xref:microsoft.quantum.intrinsic.ccnot> Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="4b439-111">Let us now compute the <xref:microsoft.quantum.intrinsic.t> depth of the <xref:microsoft.quantum.intrinsic.ccnot> operation.</span></span> <span data-ttu-id="4b439-112">Der folgende f #-Beispielcode wird verwendet:</span><span class="sxs-lookup"><span data-stu-id="4b439-112">We will use the following Q# sample code:</span></span>

```qsharp
open Microsoft.Quantum.Intrinsic;

operation ApplySampleWithCCNOT() : Unit {
    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    }
}
```

## <a name="using-depth-counter-within-a-c-program"></a><span data-ttu-id="4b439-113">Verwenden des tiefen Zählers innerhalb eines c#-Programms</span><span class="sxs-lookup"><span data-stu-id="4b439-113">Using Depth Counter within a C# Program</span></span>

<span data-ttu-id="4b439-114">Um zu überprüfen, ob `CCNOT` `T` die Tiefe 5 hat und `ApplySampleWithCCNOT` `T` die Tiefe 6 aufweist, können wir den folgenden c#-Code verwenden:</span><span class="sxs-lookup"><span data-stu-id="4b439-114">To check that `CCNOT` has `T` depth 5 and `ApplySampleWithCCNOT` has `T` depth 6 we can use the following C# code:</span></span>

```csharp
using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;
using System.Diagnostics;
var config = new QCTraceSimulatorConfiguration();
config.useDepthCounter = true;
var sim = new QCTraceSimulator(config);
var res = ApplySampleWithCCNOT.Run(sim).Result;

double tDepth = sim.GetMetric<Intrinsic.CCNOT, ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
double tDepthAll = sim.GetMetric<ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
```

<span data-ttu-id="4b439-115">Der erste Teil des Programms wird ausgeführt `ApplySampleWithCCNOT` .</span><span class="sxs-lookup"><span data-stu-id="4b439-115">The first part of the program executes `ApplySampleWithCCNOT`.</span></span> <span data-ttu-id="4b439-116">Im zweiten Teil wird die-Methode verwendet, `QCTraceSimulator.GetMetric` um die `T` Tiefe von und zu erhalten `CCNOT` `ApplySampleWithCCNOT` :</span><span class="sxs-lookup"><span data-stu-id="4b439-116">In the second part, we use the method `QCTraceSimulator.GetMetric` to get the `T` depth of `CCNOT` and `ApplySampleWithCCNOT`:</span></span> 

```csharp
double tDepth = sim.GetMetric<Intrinsic.CCNOT, ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
double tDepthAll = sim.GetMetric<ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
```

<span data-ttu-id="4b439-117">Zum Schluss können Sie, um alle im CSV-Format gesammelten Statistiken auszugeben, `Depth Counter` Folgendes verwenden:</span><span class="sxs-lookup"><span data-stu-id="4b439-117">Finally, to output all the statistics collected by `Depth Counter` in CSV format we can use the following:</span></span>
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.depthCounter];
```

## <a name="see-also"></a><span data-ttu-id="4b439-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4b439-118">See also</span></span> ##

- <span data-ttu-id="4b439-119">Übersicht über den Ablauf [Verfolgungs Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) für Quantum-Computer</span><span class="sxs-lookup"><span data-stu-id="4b439-119">The quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>

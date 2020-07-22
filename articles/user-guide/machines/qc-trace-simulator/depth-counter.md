---
title: Tiefen Counter-Quantum Development Kit
description: 'Erfahren Sie mehr über den Microsoft QDK-tiefen Zähler, der den Quantum-Ablauf Verfolgungs Simulator verwendet, um die Anzahl der einzelnen in einem Q #-Programm aufgerufenen Vorgänge zu erfassen.'
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.depth-counter
ms.openlocfilehash: 811e387fedf547d2681518ae0bb525c13dc84ff4
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/21/2020
ms.locfileid: "86871126"
---
# <a name="quantum-trace-simulator-depth-counter"></a><span data-ttu-id="eddad-103">Quantum-Ablauf Verfolgungs Simulator: tiefen Counter</span><span class="sxs-lookup"><span data-stu-id="eddad-103">Quantum trace simulator: depth counter</span></span>

<span data-ttu-id="eddad-104">Der tiefen Counter ist Teil des quantumlaufverfolgungs- [Simulators](xref:microsoft.quantum.machines.qc-trace-simulator.intro)für Quantum Development Kit.</span><span class="sxs-lookup"><span data-stu-id="eddad-104">The depth counter is a part of the Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span>
<span data-ttu-id="eddad-105">Sie können es zum Erfassen von Anzahlen verwenden, die die untere Grenze der Tiefe jedes in einem Quantum-Programm aufgerufenen Vorgangs darstellen.</span><span class="sxs-lookup"><span data-stu-id="eddad-105">You can use it to gather counts that represent the lower bound of the depth of every operation invoked in a quantum program.</span></span> 

## <a name="depth-values"></a><span data-ttu-id="eddad-106">Tiefen Werte</span><span class="sxs-lookup"><span data-stu-id="eddad-106">Depth values</span></span>

<span data-ttu-id="eddad-107">Standardmäßig haben alle Vorgänge eine Tiefe von **0** (null), mit Ausnahme des `T` Vorgangs mit einer Tiefe von **1**.</span><span class="sxs-lookup"><span data-stu-id="eddad-107">By default, all operations have a depth of **0** except the `T` operation, which has a depth of **1**.</span></span> <span data-ttu-id="eddad-108">Dies bedeutet, dass standardmäßig nur die `T` Tiefe der Vorgänge berechnet wird (was häufig wünschenswert ist).</span><span class="sxs-lookup"><span data-stu-id="eddad-108">This means that by default, only the `T` depth of operations is computed (which is often desirable).</span></span> <span data-ttu-id="eddad-109">Der tiefen Counter aggregiert und sammelt Statistiken über alle Ränder des [Aufruf Diagramms](https://en.wikipedia.org/wiki/Call_graph)des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="eddad-109">The depth counter aggregates and collects statistics over all the edges of the operation's [call graph](https://en.wikipedia.org/wiki/Call_graph).</span></span>

<span data-ttu-id="eddad-110">Alle <xref:microsoft.quantum.intrinsic> Vorgänge werden in Form von Single-Qubit-Drehungen, <xref:microsoft.quantum.intrinsic.t> Vorgängen, einzelqubit-Clifford-Vorgängen, <xref:microsoft.quantum.intrinsic.cnot> Vorgängen und Messungen von Multi-Qubit-,-Observables ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="eddad-110">All <xref:microsoft.quantum.intrinsic> operations are expressed in terms of single-qubit rotations, <xref:microsoft.quantum.intrinsic.t> operations, single-qubit Clifford operations, <xref:microsoft.quantum.intrinsic.cnot> operations, and measurements of multi-qubit Pauli observables.</span></span> <span data-ttu-id="eddad-111">Benutzer können die Tiefe für jeden der primitiven Vorgänge über das- `gateTimes` Feld von festlegen <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> .</span><span class="sxs-lookup"><span data-stu-id="eddad-111">Users can set the depth for each of the primitive operations via the `gateTimes` field of <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration>.</span></span>

## <a name="invoking-the-depth-counter"></a><span data-ttu-id="eddad-112">Aufrufen des tiefen Zählers</span><span class="sxs-lookup"><span data-stu-id="eddad-112">Invoking the depth counter</span></span>

<span data-ttu-id="eddad-113">Zum Ausführen des Quantum-Ablauf Verfolgungs Simulators mit dem tiefen Counter müssen Sie eine <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> -Instanz erstellen, die zugehörige `UseDepthCounter` -Eigenschaft auf **true**festlegen und dann eine neue- <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> Instanz mit `QCTraceSimulatorConfiguration` als Parameter erstellen.</span><span class="sxs-lookup"><span data-stu-id="eddad-113">To run the quantum trace simulator with the depth counter, you must create a <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> instance, set its `UseDepthCounter` property to **true**, and then create a new <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> instance with `QCTraceSimulatorConfiguration` as the parameter.</span></span> 

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UseDepthCounter = true;
var sim = new QCTraceSimulator(config);
```

## <a name="using-the-depth-counter-in-a-c-host-program"></a><span data-ttu-id="eddad-114">Verwenden des tiefen Zählers in einem c#-Host Programm</span><span class="sxs-lookup"><span data-stu-id="eddad-114">Using the depth counter in a C# host program</span></span>

<span data-ttu-id="eddad-115">Das c#-Beispiel, das in diesem Abschnitt folgt, berechnet die `T` Tiefe des `CCNOT` Vorgangs basierend auf dem folgenden f #-Beispielcode:</span><span class="sxs-lookup"><span data-stu-id="eddad-115">The C# example that follows in this section computes the `T` depth of the `CCNOT` operation, based on the following Q# sample code:</span></span>

```qsharp
open Microsoft.Quantum.Intrinsic;

operation ApplySampleWithCCNOT() : Unit {
    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    }
}
```

<span data-ttu-id="eddad-116">Verwenden Sie den folgenden c#-Code, um zu überprüfen, ob die `CCNOT` `T` Tiefe **5** und `ApplySampleWithCCNOT` `T` die Tiefe **6**hat:</span><span class="sxs-lookup"><span data-stu-id="eddad-116">To check that `CCNOT` has `T` depth **5** and `ApplySampleWithCCNOT` has `T` depth **6**, use the following C# code:</span></span>

```csharp
using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;
using System.Diagnostics;
var config = new QCTraceSimulatorConfiguration();
config.UseDepthCounter = true;
var sim = new QCTraceSimulator(config);
var res = ApplySampleWithCCNOT.Run(sim).Result;

double tDepth = sim.GetMetric<Intrinsic.CCNOT, ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
double tDepthAll = sim.GetMetric<ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
```

<span data-ttu-id="eddad-117">Der erste Teil des Programms wird ausgeführt `ApplySampleWithCCNOT` .</span><span class="sxs-lookup"><span data-stu-id="eddad-117">The first part of the program runs `ApplySampleWithCCNOT`.</span></span> <span data-ttu-id="eddad-118">Im zweiten Teil wird die [`GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) -Methode verwendet, um die `T` Tiefe von `CCNOT` und abzurufen `ApplySampleWithCCNOT` .</span><span class="sxs-lookup"><span data-stu-id="eddad-118">The second part uses the [`GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) method to retrieve the `T` depth of `CCNOT` and `ApplySampleWithCCNOT`.</span></span> 

<span data-ttu-id="eddad-119">Zum Schluss können Sie mithilfe der folgenden Informationen alle vom tiefen Leistungs befassenden Statistiken im CSV-Format ausgeben:</span><span class="sxs-lookup"><span data-stu-id="eddad-119">Finally, you can output all the statistics collected by the depth counter in CSV format using the following:</span></span>
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.depthCounter];
```

## <a name="see-also"></a><span data-ttu-id="eddad-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="eddad-120">See also</span></span>

- <span data-ttu-id="eddad-121">Übersicht über den Quantum Development Kit [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) .</span><span class="sxs-lookup"><span data-stu-id="eddad-121">The Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
- <span data-ttu-id="eddad-122">Die <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API-Referenz.</span><span class="sxs-lookup"><span data-stu-id="eddad-122">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API reference.</span></span>
- <span data-ttu-id="eddad-123">Die <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API-Referenz.</span><span class="sxs-lookup"><span data-stu-id="eddad-123">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API reference.</span></span>
- <span data-ttu-id="eddad-124">Die <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.MetricsNames.DepthCounter> API-Referenz.</span><span class="sxs-lookup"><span data-stu-id="eddad-124">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.MetricsNames.DepthCounter> API reference.</span></span>

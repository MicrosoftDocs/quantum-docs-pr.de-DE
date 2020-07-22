---
title: Primitiver Vorgangs Counter-Quantum Development Kit
description: 'Erfahren Sie mehr über den "Microsoft QDK primitive Operation"-Vorgang, der den Quantum Trace-Simulator verwendet, um primitive Ausführungen zu verfolgen, die von Vorgängen in einem Q #-Programm'
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.primitive-counter
ms.openlocfilehash: ea022d499354f7cefd60da690466496e0ce7c336
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/21/2020
ms.locfileid: "86871024"
---
# <a name="quantum-trace-simulator-primitive-operations-counter"></a><span data-ttu-id="b97fc-103">Quantum-Ablauf Verfolgungs Simulator: primitiver Vorgangs Counter</span><span class="sxs-lookup"><span data-stu-id="b97fc-103">Quantum trace simulator: primitive operations counter</span></span>

<span data-ttu-id="b97fc-104">Der primitive Vorgangs Counter ist Teil des Quantum Development Kit- [quantumlaufverfolgungs-Simulators](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span><span class="sxs-lookup"><span data-stu-id="b97fc-104">The primitive operation counter is a part of the Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span> <span data-ttu-id="b97fc-105">Sie zählt die Anzahl primitiver Ausführungen, die von jedem in einem Quantum-Programm aufgerufenen Vorgang verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b97fc-105">It counts the number of primitive executions used by every operation invoked in a quantum program.</span></span> 

<span data-ttu-id="b97fc-106">Alle <xref:microsoft.quantum.intrinsic> Vorgänge werden in Form von Single-Qubit-Drehungen, T-Vorgängen, Single-Qubit-Clifford-Vorgängen, CNOT-Vorgängen und Messungen von Multi-Qubit--Observables ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="b97fc-106">All <xref:microsoft.quantum.intrinsic> operations are expressed in terms of single-qubit rotations, T operations, single-qubit Clifford operations, CNOT operations, and measurements of multi-qubit Pauli observables.</span></span> <span data-ttu-id="b97fc-107">Der primitive Vorgangs Vergleich aggregiert und sammelt Statistiken über alle Ränder des [Aufruf Diagramms](https://en.wikipedia.org/wiki/Call_graph)des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="b97fc-107">The Primitive Operations Counter aggregates and collects statistics over all the edges of the operation's [call graph](https://en.wikipedia.org/wiki/Call_graph).</span></span>

## <a name="invoking-the-primitive-operation-counter"></a><span data-ttu-id="b97fc-108">Aufruf des primitiven Vorgangs Zählers</span><span class="sxs-lookup"><span data-stu-id="b97fc-108">Invoking the primitive operation counter</span></span>

<span data-ttu-id="b97fc-109">Sie müssen eine- <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> Instanz erstellen, die `UsePrimitiveOperationsCounter` -Eigenschaft auf **true**festlegen und dann eine neue- <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> Instanz mit `QCTraceSimulatorConfiguration` als Parameter erstellen, um den Quantum-Ablauf Verfolgungs Simulator mit dem Wert für den primitiven Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="b97fc-109">To run the quantum trace simulator with the primitive operation counter, you must create a <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> instance, set the `UsePrimitiveOperationsCounter` property to **true**, and then create a new <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> instance with the `QCTraceSimulatorConfiguration` as the parameter.</span></span>

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UsePrimitiveOperationsCounter = true;
var sim = new QCTraceSimulator(config);
```

## <a name="using-the-primitive-operation-counter-in-a-c-host-program"></a><span data-ttu-id="b97fc-110">Verwendung des primitiven Vorgangs Zählers in einem c#-Host Programm</span><span class="sxs-lookup"><span data-stu-id="b97fc-110">Using the primitive operation counter in a C# host program</span></span>

<span data-ttu-id="b97fc-111">Das c#-Beispiel in diesem Abschnitt zählt, wie viele <xref:microsoft.quantum.intrinsic.t> Vorgänge zum Implementieren des Vorgangs erforderlich sind <xref:microsoft.quantum.intrinsic.ccnot> , basierend auf dem folgenden f #-Beispielcode:</span><span class="sxs-lookup"><span data-stu-id="b97fc-111">The C# example that follows in this section counts how many <xref:microsoft.quantum.intrinsic.t> operations are needed to implement the <xref:microsoft.quantum.intrinsic.ccnot> operation, based on the following Q# sample code:</span></span>

```qsharp
open Microsoft.Quantum.Intrinsic;
operation ApplySampleWithCCNOT() : Unit {

    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    }
}
```

<span data-ttu-id="b97fc-112">Verwenden Sie den folgenden c#-Code, um zu überprüfen, ob `CCNOT` sieben `T` Vorgänge erforderlich sind und dass `ApplySampleWithCCNOT` acht `T` Vorgänge ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="b97fc-112">To check that `CCNOT` requires seven `T` operations and that `ApplySampleWithCCNOT` runs eight `T` operations, use the following C# code:</span></span>

```csharp 
// using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;
// using System.Diagnostics;
var config = new QCTraceSimulatorConfiguration();
config.UsePrimitiveOperationsCounter = true;
var sim = new QCTraceSimulator(config);
var res = ApplySampleWithCCNOT.Run(sim).Result;

double tCountAll = sim.GetMetric<ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
double tCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
```

<span data-ttu-id="b97fc-113">Der erste Teil des Programms wird ausgeführt `ApplySampleWithCCNOT` .</span><span class="sxs-lookup"><span data-stu-id="b97fc-113">The first part of the program runs `ApplySampleWithCCNOT`.</span></span> <span data-ttu-id="b97fc-114">Im zweiten Teil wird die- [`QCTraceSimulator.GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) Methode verwendet, um die Anzahl der Vorgänge abzurufen, die `T` von ausgeführt werden `ApplySampleWithCCNOT` :</span><span class="sxs-lookup"><span data-stu-id="b97fc-114">The second part uses the [`QCTraceSimulator.GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) method to retrieve the number of `T` operations run by `ApplySampleWithCCNOT`:</span></span> 

<span data-ttu-id="b97fc-115">Wenn Sie `GetMetric` mit zwei Typparametern aufzurufen, wird der Wert der Metrik zurückgegeben, die einem angegebenen Aufruf Diagramm Rand zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b97fc-115">When you call `GetMetric` with two type parameters, it returns the value of the metric associated with a given call graph edge.</span></span> <span data-ttu-id="b97fc-116">Im vorherigen Beispiel ruft das Programm den `Primitive.CCNOT` -Vorgang innerhalb von auf `ApplySampleWithCCNOT` . Daher enthält das Aufruf Diagramm den Edge `<Primitive.CCNOT, ApplySampleWithCCNOT>` .</span><span class="sxs-lookup"><span data-stu-id="b97fc-116">In the preceding example, the program calls the `Primitive.CCNOT` operation  within `ApplySampleWithCCNOT` and therefore the call graph contains the edge `<Primitive.CCNOT, ApplySampleWithCCNOT>`.</span></span> 

<span data-ttu-id="b97fc-117">Um die Anzahl der `CNOT` verwendeten Vorgänge abzurufen, fügen Sie die folgende Zeile hinzu:</span><span class="sxs-lookup"><span data-stu-id="b97fc-117">To retrieve the number of `CNOT` operations used, add the following line:</span></span>
```csharp
double cxCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.CX);
```

<span data-ttu-id="b97fc-118">Zum Schluss können Sie mithilfe der folgenden Daten alle vom primitiven Betriebs Leistungs-Leistungsdaten erfassten Statistiken im CSV-Format ausgeben:</span><span class="sxs-lookup"><span data-stu-id="b97fc-118">Finally, you can output all the statistics collected by the Primitive Operations Counter in CSV format using the following:</span></span>
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.primitiveOperationsCounter];
```

## <a name="see-also"></a><span data-ttu-id="b97fc-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b97fc-119">See also</span></span>

- <span data-ttu-id="b97fc-120">Übersicht über den Quantum Development Kit [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) .</span><span class="sxs-lookup"><span data-stu-id="b97fc-120">The Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
- <span data-ttu-id="b97fc-121">Die <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API-Referenz.</span><span class="sxs-lookup"><span data-stu-id="b97fc-121">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API reference.</span></span>
- <span data-ttu-id="b97fc-122">Die <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API-Referenz.</span><span class="sxs-lookup"><span data-stu-id="b97fc-122">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API reference.</span></span>
- <span data-ttu-id="b97fc-123">Die <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.PrimitiveOperationsGroupsNames> API-Referenz.</span><span class="sxs-lookup"><span data-stu-id="b97fc-123">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.PrimitiveOperationsGroupsNames> API reference.</span></span>
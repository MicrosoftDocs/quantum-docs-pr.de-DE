---
title: Primitiver Vorgangs-Counter | Ablauf Verfolgungs Simulator für Quantum-Computer | Microsoft-Dokumentation
description: Übersicht über Ablaufverfolgungssimulator für Quantencomputer
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.primitive-counter
ms.openlocfilehash: 1f554c0a1b92c8f6b59be3a9d9965e0e25bd074f
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "76820418"
---
# <a name="primitive-operations-counter"></a><span data-ttu-id="329e7-103">Primitiver Vorgangs-Counter</span><span class="sxs-lookup"><span data-stu-id="329e7-103">Primitive Operations Counter</span></span>  

<span data-ttu-id="329e7-104">Der `Primitive Operations Counter` ist Teil des Ablauf [Verfolgungs Simulators](xref:microsoft.quantum.machines.qc-trace-simulator.intro)für Quantum-Computer.</span><span class="sxs-lookup"><span data-stu-id="329e7-104">The `Primitive Operations Counter` is a part of the quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span> <span data-ttu-id="329e7-105">Sie zählt die Anzahl primitiver Ausführungen, die von jedem in einem Quantum-Programm aufgerufenen Vorgang verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="329e7-105">It counts the number of primitive executions used by every operation invoked in a quantum program.</span></span> <span data-ttu-id="329e7-106">Alle Vorgänge aus `Microsoft.Quantum.Intrinsic` werden in Form einzelner Qubit-Drehungen, t Gates, einzelner Qubit Clifford Gates, CNOT Gates und Messungen von Multi-Qubit Pauli Observables ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="329e7-106">All operations from `Microsoft.Quantum.Intrinsic` are expressed in terms of single qubit rotations, T gates, single qubit Clifford gates, CNOT gates and measurements of multi-qubit Pauli observables.</span></span> <span data-ttu-id="329e7-107">Gesammelte Statistiken werden über die Ränder des Vorgangs Aufruf Diagramms aggregiert.</span><span class="sxs-lookup"><span data-stu-id="329e7-107">Collected statistics are aggregated over the edges of the operations call graph.</span></span> <span data-ttu-id="329e7-108">Wir zählen nun, wie viele `T` Gates zum Implementieren des `CCNOT` Vorgangs benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="329e7-108">Let us now count how many `T` gates are needed to implement the `CCNOT` operation.</span></span> 

```qsharp
open Microsoft.Quantum.Intrinsic;
operation ApplySampleWithCCNOT() : Unit {

    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    } 
}
```

## <a name="using-the-primitive-operations-counter-within-a-c-program"></a><span data-ttu-id="329e7-109">Verwenden des "primitive"-Vorgangs C# Zählers innerhalb eines Programms</span><span class="sxs-lookup"><span data-stu-id="329e7-109">Using the Primitive Operations Counter within a C# Program</span></span>

<span data-ttu-id="329e7-110">Um zu überprüfen, ob `CCNOT` tatsächlich 7 `T` Gates erfordert und `ApplySampleWithCCNOT` 8 `T` Gates ausführt, können wir C# den folgenden Code verwenden:</span><span class="sxs-lookup"><span data-stu-id="329e7-110">To check that `CCNOT` indeed requires 7 `T` gates and that `ApplySampleWithCCNOT` executes 8 `T` gates we can use the following C# code:</span></span>

```csharp 
// using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;
// using System.Diagnostics;
var config = new QCTraceSimulatorConfiguration();
config.usePrimitiveOperationsCounter = true;
var sim = new QCTraceSimulator(config);
var res = ApplySampleWithCCNOT.Run(sim).Result;

double tCountAll = sim.GetMetric<ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
double tCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
```

<span data-ttu-id="329e7-111">Der erste Teil des Programms führt `ApplySampleWithCCNOT`aus.</span><span class="sxs-lookup"><span data-stu-id="329e7-111">The first part of the program executes `ApplySampleWithCCNOT`.</span></span> <span data-ttu-id="329e7-112">Im zweiten Teil verwenden wir die-Methode `QCTraceSimulator.GetMetric`, um die Anzahl von t Gates zu erhalten, die von `ApplySampleWithCCNOT`ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="329e7-112">In the second part, we use the method `QCTraceSimulator.GetMetric` to get the number of T gates executed by `ApplySampleWithCCNOT`:</span></span> 

```csharp
double tCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
double tCountAll = sim.GetMetric<ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
```

<span data-ttu-id="329e7-113">Wenn `GetMetric` mit zwei Typparametern aufgerufen wird, wird der Wert der Metrik zurückgegeben, die einem angegebenen Aufruf Diagramm Rand zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="329e7-113">When `GetMetric` is called with two type parameters it returns the value of the metric associated with a given call graph edge.</span></span> <span data-ttu-id="329e7-114">In unserem Beispiel Vorgang wird `Primitive.CCNOT` in `ApplySampleWithCCNOT` aufgerufen, und das Aufruf Diagramm enthält daher die Edge-`<Primitive.CCNOT, ApplySampleWithCCNOT>`.</span><span class="sxs-lookup"><span data-stu-id="329e7-114">In our example operation `Primitive.CCNOT` is called within `ApplySampleWithCCNOT` and therefore the call graph contains the edge `<Primitive.CCNOT, ApplySampleWithCCNOT>`.</span></span> 

<span data-ttu-id="329e7-115">Um die Anzahl der verwendeten `CNOT` Gates zu erhalten, können Sie die folgende Zeile hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="329e7-115">To get the number of `CNOT` gates used, we can add the following line:</span></span>
```csharp
double cxCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.CX);
```

<span data-ttu-id="329e7-116">Schließlich können Sie Folgendes verwenden, um alle Statistiken auszugeben, die vom Gate-Counter im CSV-Format erfasst wurden:</span><span class="sxs-lookup"><span data-stu-id="329e7-116">Finally, to output all the statistics collected by the gate counter in CSV format we can use the following:</span></span>
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.primitiveOperationsCounter];
```

## <a name="see-also"></a><span data-ttu-id="329e7-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="329e7-117">See also</span></span> ##

- <span data-ttu-id="329e7-118">Übersicht über den Ablauf [Verfolgungs Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) für Quantum-Computer</span><span class="sxs-lookup"><span data-stu-id="329e7-118">The quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>

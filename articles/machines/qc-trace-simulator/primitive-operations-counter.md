---
title: Primitiver Vorgangs-Counter | Ablauf Verfolgungs Simulator für Quantum-Computer | Microsoft-Dokumentation
description: Übersicht über den Ablauf Verfolgungs Simulator für Quantum-Computer
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.primitive-counter
ms.openlocfilehash: b7ec8b0d7a713051e36cb778c087050f0257710f
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/29/2019
ms.locfileid: "73184881"
---
# <a name="primitive-operations-counter"></a><span data-ttu-id="532a0-103">Primitiver Vorgangs-Counter</span><span class="sxs-lookup"><span data-stu-id="532a0-103">Primitive Operations Counter</span></span>  

<span data-ttu-id="532a0-104">Der `Primitive Operations Counter` ist Teil des Ablauf [Verfolgungs Simulators](xref:microsoft.quantum.machines.qc-trace-simulator.intro)für Quantum-Computer.</span><span class="sxs-lookup"><span data-stu-id="532a0-104">The `Primitive Operations Counter` is a part of the quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span> <span data-ttu-id="532a0-105">Sie zählt die Anzahl primitiver Ausführungen, die von jedem in einem Quantum-Programm aufgerufenen Vorgang verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="532a0-105">It counts the number of primitive executions used by every operation invoked in a quantum program.</span></span> <span data-ttu-id="532a0-106">Alle Vorgänge aus `Microsoft.Quantum.Primitive` werden in Form einzelner Qubit-Drehungen, t Gates, einzelner Qubit Clifford Gates, CNOT Gates und Messungen von Multi-Qubit Pauli Observables ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="532a0-106">All operations from `Microsoft.Quantum.Primitive` are expressed in terms of single qubit rotations, T gates, single qubit Clifford gates, CNOT gates and measurements of multi-qubit Pauli observables.</span></span> <span data-ttu-id="532a0-107">Gesammelte Statistiken werden über die Ränder des Vorgangs Aufruf Diagramms aggregiert.</span><span class="sxs-lookup"><span data-stu-id="532a0-107">Collected statistics are aggregated over the edges of the operations call graph.</span></span> <span data-ttu-id="532a0-108">Wir zählen nun, wie viele `T` Gates zum Implementieren des `CCNOT` Vorgangs benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="532a0-108">Let us now count how many `T` gates are needed to implement the `CCNOT` operation.</span></span> 

```qsharp
open Microsoft.Quantum.Primitive;
operation CCNOTDriver() : Unit {

    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    } 
}
```

## <a name="using-the-primitive-operations-counter-within-a-c-program"></a><span data-ttu-id="532a0-109">Verwenden des "primitive"-Vorgangs C# Zählers innerhalb eines Programms</span><span class="sxs-lookup"><span data-stu-id="532a0-109">Using the Primitive Operations Counter within a C# Program</span></span>

<span data-ttu-id="532a0-110">Um zu überprüfen, ob `CCNOT` tatsächlich 7 `T` Gates erfordert und `CCNOTDriver` 8 `T` Gates ausführt, können wir C# den folgenden Code verwenden:</span><span class="sxs-lookup"><span data-stu-id="532a0-110">To check that `CCNOT` indeed requires 7 `T` gates and that `CCNOTDriver` executes 8 `T` gates we can use the following C# code:</span></span>

```csharp 
// using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;
// using System.Diagnostics;
var config = new QCTraceSimulatorConfiguration();
config.usePrimitiveOperationsCounter = true;
var sim = new QCTraceSimulator(config);
var res = CCNOTDriver.Run(sim).Result;

double tCountAll = sim.GetMetric<CCNOTDriver>(PrimitiveOperationsGroupsNames.T);
double tCount = sim.GetMetric<Primitive.CCNOT, CCNOTDriver>(PrimitiveOperationsGroupsNames.T);
```

<span data-ttu-id="532a0-111">Der erste Teil des Programms führt `CCNOTDriver`aus.</span><span class="sxs-lookup"><span data-stu-id="532a0-111">The first part of the program executes `CCNOTDriver`.</span></span> <span data-ttu-id="532a0-112">Im zweiten Teil verwenden wir die-Methode `QCTraceSimulator.GetMetric`, um die Anzahl von t Gates zu erhalten, die von `CCNOTDriver`ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="532a0-112">In the second part, we use the method `QCTraceSimulator.GetMetric` to get the number of T gates executed by `CCNOTDriver`:</span></span> 

```csharp
double tCount = sim.GetMetric<Primitive.CCNOT, CCNOTDriver>(PrimitiveOperationsGroupsNames.T);
double tCountAll = sim.GetMetric<CCNOTDriver>(PrimitiveOperationsGroupsNames.T);
```

<span data-ttu-id="532a0-113">Wenn `GetMetric` mit zwei Typparametern aufgerufen wird, wird der Wert der Metrik zurückgegeben, die einem angegebenen Aufruf Diagramm Rand zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="532a0-113">When `GetMetric` is called with two type parameters it returns the value of the metric associated with a given call graph edge.</span></span> <span data-ttu-id="532a0-114">In unserem Beispiel Vorgang wird `Primitive.CCNOT` in `CCNOTDriver` aufgerufen, und das Aufruf Diagramm enthält daher die Edge-`<Primitive.CCNOT,CCNOTDriver>`.</span><span class="sxs-lookup"><span data-stu-id="532a0-114">In our example operation `Primitive.CCNOT` is called within `CCNOTDriver` and therefore the call graph contains the edge `<Primitive.CCNOT,CCNOTDriver>`.</span></span> 

<span data-ttu-id="532a0-115">Um die Anzahl der verwendeten `CNOT` Gates zu erhalten, können Sie die folgende Zeile hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="532a0-115">To get the number of `CNOT` gates used, we can add the following line:</span></span>
```csharp
double cxCount = sim.GetMetric<Primitive.CCNOT, CCNOTDriver>(PrimitiveOperationsGroupsNames.CX);
```

<span data-ttu-id="532a0-116">Schließlich können Sie Folgendes verwenden, um alle Statistiken auszugeben, die vom Gate-Counter im CSV-Format erfasst wurden:</span><span class="sxs-lookup"><span data-stu-id="532a0-116">Finally, to output all the statistics collected by the gate counter in CSV format we can use the following:</span></span>
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.primitiveOperationsCounter];
```

## <a name="see-also"></a><span data-ttu-id="532a0-117">Informationen finden Sie auch unter</span><span class="sxs-lookup"><span data-stu-id="532a0-117">See also</span></span> ##

- <span data-ttu-id="532a0-118">Übersicht über den Ablauf [Verfolgungs Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) für Quantum-Computer</span><span class="sxs-lookup"><span data-stu-id="532a0-118">The quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>

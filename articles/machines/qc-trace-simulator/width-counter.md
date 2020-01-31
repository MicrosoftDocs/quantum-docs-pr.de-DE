---
title: Breiten-Counter | Ablauf Verfolgungs Simulator für Quantum-Computer | Microsoft-Dokumentation
description: Übersicht über Ablaufverfolgungssimulator für Quantencomputer
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.width-counter
ms.openlocfilehash: 9c3601e74eec17bd6b463e90f8f3085c959d6f95
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "76820367"
---
# <a name="width-counter"></a><span data-ttu-id="453b6-103">Breiten-Counter</span><span class="sxs-lookup"><span data-stu-id="453b6-103">Width Counter</span></span>

<span data-ttu-id="453b6-104">Der `Width Counter` zählt die Anzahl der von jedem Vorgang zugeordneten und zugeordneten Qubits.</span><span class="sxs-lookup"><span data-stu-id="453b6-104">The `Width Counter` counts the number of qubits allocated and borrowed by each operation.</span></span>
<span data-ttu-id="453b6-105">Alle Vorgänge aus dem `Microsoft.Quantum.Intrinsic`-Namespace werden in Form einzelner Qubit-Drehungen, t Gates, einzelner Qubit Clifford Gates, CNOT Gates und Messungen von Multi-Qubit Pauli Observables ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="453b6-105">All operations from the `Microsoft.Quantum.Intrinsic` namespace are expressed in terms of single qubit rotations, T gates, single qubit Clifford gates, CNOT gates and measurements of multi-qubit Pauli observables.</span></span> <span data-ttu-id="453b6-106">Einige der primitiven Vorgänge können zusätzliche Qubits zuordnen.</span><span class="sxs-lookup"><span data-stu-id="453b6-106">Some of the primitive operations can allocate extra qubits.</span></span> <span data-ttu-id="453b6-107">Multiplizieren Sie z. b. die kontrollierten `X` Gates oder kontrollierten `T` Gates.</span><span class="sxs-lookup"><span data-stu-id="453b6-107">For example, multiply controlled `X` gates or controlled `T` gates.</span></span> <span data-ttu-id="453b6-108">Wir berechnen die Anzahl der zusätzlichen Qubits, die durch die Implementierung eines Multiplikations gesteuerten `X` Gates zugeordnet werden:</span><span class="sxs-lookup"><span data-stu-id="453b6-108">Let us compute the number of extra qubits allocated by the implementation of a multiply controlled `X` gate:</span></span>

```qsharp
open Microsoft.Quantum.Intrinsic;
open Microsoft.Quantum.Arrays;
operation ApplyMultiControlledX( numberOfQubits : Int ) : Unit {
    using(qubits = Qubit[numberOfQubits]) {
        Controlled X (Rest(qubits), Head(qubits));
    } 
}
```

## <a name="using-width-counter-within-a-c-program"></a><span data-ttu-id="453b6-109">Verwenden des Width-Zählers innerhalb eines C# Programms</span><span class="sxs-lookup"><span data-stu-id="453b6-109">Using Width Counter within a C# Program</span></span>

<span data-ttu-id="453b6-110">Bei der multiplizierten `X`, die auf insgesamt 5 Qubits wirkt, werden zwei hilfskbits und die Eingabe Breite 5 verwendet.</span><span class="sxs-lookup"><span data-stu-id="453b6-110">Multiply controlled `X` acting on a total of 5 qubits will allocate 2 ancillary qubits and its input width will be 5.</span></span> <span data-ttu-id="453b6-111">Um zu überprüfen, ob dies der Fall ist, können wir C# Folgendes Programm verwenden:</span><span class="sxs-lookup"><span data-stu-id="453b6-111">To check that this is the case, we can use the following C# program:</span></span>

```csharp 
var config = new QCTraceSimulatorConfiguration();
config.useWidthCounter = true;
var sim = new QCTraceSimulator(config);
int totalNumberOfQubits = 5;
var res = ApplyMultiControlledX.Run(sim, totalNumberOfQubits).Result;

double allocatedQubits = 
    sim.GetMetric<Primitive.X, ApplyMultiControlledX>(
        WidthCounter.Metrics.ExtraWidth,
        functor: OperationFunctor.Controlled); 

double inputWidth =
    sim.GetMetric<Primitive.X, ApplyMultiControlledX>(
        WidthCounter.Metrics.InputWidth,
        functor: OperationFunctor.Controlled);
```

<span data-ttu-id="453b6-112">Der erste Teil des Programms führt `ApplyMultiControlledX`aus.</span><span class="sxs-lookup"><span data-stu-id="453b6-112">The first part of the program executes `ApplyMultiControlledX`.</span></span> <span data-ttu-id="453b6-113">Im zweiten Teil verwenden wir die-Methode `QCTraceSimulator.GetMetric`, um die Anzahl der zugeordneten Qubits abzurufen, sowie die Anzahl der Qubits, die `X` als Eingabe empfangen haben.</span><span class="sxs-lookup"><span data-stu-id="453b6-113">In the second part we use the method `QCTraceSimulator.GetMetric` to get the number of allocated qubits as well as the number of qubits that Controlled `X` received as input.</span></span> 

<span data-ttu-id="453b6-114">Zum Schluss können Sie die folgenden Informationen verwenden, um alle Statistiken auszugeben, die von der Width-Zahl im CSV-Format erfasst wurden:</span><span class="sxs-lookup"><span data-stu-id="453b6-114">Finally, to output all the statistics collected by width counter in CSV format we can use the following:</span></span>
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.widthCounter];
```

## <a name="see-also"></a><span data-ttu-id="453b6-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="453b6-115">See also</span></span> ##

- <span data-ttu-id="453b6-116">Übersicht über den Ablauf [Verfolgungs Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) für Quantum-Computer</span><span class="sxs-lookup"><span data-stu-id="453b6-116">The quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>

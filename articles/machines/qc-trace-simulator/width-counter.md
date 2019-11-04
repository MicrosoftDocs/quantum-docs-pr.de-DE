---
title: Breiten-Counter | Ablauf Verfolgungs Simulator für Quantum-Computer | Microsoft-Dokumentation
description: Übersicht über den Ablauf Verfolgungs Simulator für Quantum-Computer
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.width-counter
ms.openlocfilehash: ae0c0ec2e677be03dc8dc1497dc62ad9034295a4
ms.sourcegitcommit: aa5e6f4a2deb4271a333d3f1b1eb69b5bb9a7bad
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2019
ms.locfileid: "73442415"
---
# <a name="width-counter"></a><span data-ttu-id="bad2a-103">Breiten-Counter</span><span class="sxs-lookup"><span data-stu-id="bad2a-103">Width Counter</span></span>

<span data-ttu-id="bad2a-104">Der `Width Counter` zählt die Anzahl der von jedem Vorgang zugeordneten und zugeordneten Qubits.</span><span class="sxs-lookup"><span data-stu-id="bad2a-104">The `Width Counter` counts the number of qubits allocated and borrowed by each operation.</span></span>
<span data-ttu-id="bad2a-105">Alle Vorgänge aus dem `Microsoft.Quantum.Primitive`-Namespace werden in Form einzelner Qubit-Drehungen, t Gates, einzelner Qubit Clifford Gates, CNOT Gates und Messungen von Multi-Qubit Pauli Observables ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="bad2a-105">All operations from the `Microsoft.Quantum.Primitive` namespace are expressed in terms of single qubit rotations, T gates, single qubit Clifford gates, CNOT gates and measurements of multi-qubit Pauli observables.</span></span> <span data-ttu-id="bad2a-106">Einige der primitiven Vorgänge können zusätzliche Qubits zuordnen.</span><span class="sxs-lookup"><span data-stu-id="bad2a-106">Some of the primitive operations can allocate extra qubits.</span></span> <span data-ttu-id="bad2a-107">Multiplizieren Sie z. b. die kontrollierten `X` Gates oder kontrollierten `T` Gates.</span><span class="sxs-lookup"><span data-stu-id="bad2a-107">For example, multiply controlled `X` gates or controlled `T` gates.</span></span> <span data-ttu-id="bad2a-108">Wir berechnen die Anzahl der zusätzlichen Qubits, die durch die Implementierung eines Multiplikations gesteuerten `X` Gates zugeordnet werden:</span><span class="sxs-lookup"><span data-stu-id="bad2a-108">Let us compute the number of extra qubits allocated by the implementation of a multiply controlled `X` gate:</span></span>

```qsharp
open Microsoft.Quantum.Primitive;
open Microsoft.Quantum.Arrays;
operation MultiControlledXDriver( numberOfQubits : Int ) : Unit {

    using(qubits = Qubit[numberOfQubits]) {
        Controlled X (Rest(qubits), Head(qubits));
    } 
}
```

## <a name="using-width-counter-within-a-c-program"></a><span data-ttu-id="bad2a-109">Verwenden des Width-Zählers innerhalb eines C# Programms</span><span class="sxs-lookup"><span data-stu-id="bad2a-109">Using Width Counter within a C# Program</span></span>

<span data-ttu-id="bad2a-110">Bei der multiplizierten `X`, die auf insgesamt 5 Qubits wirkt, werden zwei hilfskbits und die Eingabe Breite 5 verwendet.</span><span class="sxs-lookup"><span data-stu-id="bad2a-110">Multiply controlled `X` acting on a total of 5 qubits will allocate 2 ancillary qubits and its input width will be 5.</span></span> <span data-ttu-id="bad2a-111">Um zu überprüfen, ob dies der Fall ist, können wir C# Folgendes Programm verwenden:</span><span class="sxs-lookup"><span data-stu-id="bad2a-111">To check that this is the case, we can use the following C# program:</span></span>

```csharp 
var config = new QCTraceSimulatorConfiguration();
config.useWidthCounter = true;
var sim = new QCTraceSimulator(config);
int totalNumberOfQubits = 5;
var res = MultiControlledXDriver.Run(sim, totalNumberOfQubits).Result;

double allocatedQubits = 
    sim.GetMetric<Primitive.X, MultiControlledXDriver>(
        WidthCounter.Metrics.ExtraWidth,
        functor: OperationFunctor.Controlled); 

double inputWidth =
    sim.GetMetric<Primitive.X, MultiControlledXDriver>(
        WidthCounter.Metrics.InputWidth,
        functor: OperationFunctor.Controlled);
```

<span data-ttu-id="bad2a-112">Der erste Teil des Programms führt `MultiControlledXDriver`aus.</span><span class="sxs-lookup"><span data-stu-id="bad2a-112">The first part of the program executes `MultiControlledXDriver`.</span></span> <span data-ttu-id="bad2a-113">Im zweiten Teil verwenden wir die-Methode `QCTraceSimulator.GetMetric`, um die Anzahl der zugeordneten Qubits abzurufen, sowie die Anzahl der Qubits, die `X` als Eingabe empfangen haben.</span><span class="sxs-lookup"><span data-stu-id="bad2a-113">In the second part we use the method `QCTraceSimulator.GetMetric` to get the number of allocated qubits as well as the number of qubits that Controlled `X` received as input.</span></span> 

<span data-ttu-id="bad2a-114">Zum Schluss können Sie die folgenden Informationen verwenden, um alle Statistiken auszugeben, die von der Width-Zahl im CSV-Format erfasst wurden:</span><span class="sxs-lookup"><span data-stu-id="bad2a-114">Finally, to output all the statistics collected by width counter in CSV format we can use the following:</span></span>
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.widthCounter];
```

## <a name="see-also"></a><span data-ttu-id="bad2a-115">Informationen finden Sie auch unter</span><span class="sxs-lookup"><span data-stu-id="bad2a-115">See also</span></span> ##

- <span data-ttu-id="bad2a-116">Übersicht über den Ablauf [Verfolgungs Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) für Quantum-Computer</span><span class="sxs-lookup"><span data-stu-id="bad2a-116">The quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>

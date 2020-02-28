---
title: Breiten-Counter
description: Erfahren Sie mehr über den Microsoft QDK Width-Zähler, der die Anzahl der von jedem Vorgang in einem Quantum-Programm zugeordneten und zugeordneten Qubits zählt.
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.width-counter
ms.openlocfilehash: a76292222950310acc90dded02980e4a5b792e76
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907085"
---
# <a name="width-counter"></a><span data-ttu-id="6bb65-103">Breiten-Counter</span><span class="sxs-lookup"><span data-stu-id="6bb65-103">Width Counter</span></span>

<span data-ttu-id="6bb65-104">Der `Width Counter` zählt die Anzahl der von jedem Vorgang zugeordneten und zugeordneten Qubits.</span><span class="sxs-lookup"><span data-stu-id="6bb65-104">The `Width Counter` counts the number of qubits allocated and borrowed by each operation.</span></span>
<span data-ttu-id="6bb65-105">Alle Vorgänge aus dem `Microsoft.Quantum.Intrinsic`-Namespace werden in Form einzelner Qubit-Drehungen, t Gates, einzelner Qubit Clifford Gates, CNOT Gates und Messungen von Multi-Qubit Pauli Observables ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="6bb65-105">All operations from the `Microsoft.Quantum.Intrinsic` namespace are expressed in terms of single qubit rotations, T gates, single qubit Clifford gates, CNOT gates and measurements of multi-qubit Pauli observables.</span></span> <span data-ttu-id="6bb65-106">Einige der primitiven Vorgänge können zusätzliche Qubits zuordnen.</span><span class="sxs-lookup"><span data-stu-id="6bb65-106">Some of the primitive operations can allocate extra qubits.</span></span> <span data-ttu-id="6bb65-107">Multiplizieren Sie z. b. die kontrollierten `X` Gates oder kontrollierten `T` Gates.</span><span class="sxs-lookup"><span data-stu-id="6bb65-107">For example, multiply controlled `X` gates or controlled `T` gates.</span></span> <span data-ttu-id="6bb65-108">Wir berechnen die Anzahl der zusätzlichen Qubits, die durch die Implementierung eines Multiplikations gesteuerten `X` Gates zugeordnet werden:</span><span class="sxs-lookup"><span data-stu-id="6bb65-108">Let us compute the number of extra qubits allocated by the implementation of a multiply controlled `X` gate:</span></span>

```qsharp
open Microsoft.Quantum.Intrinsic;
open Microsoft.Quantum.Arrays;
operation ApplyMultiControlledX( numberOfQubits : Int ) : Unit {
    using(qubits = Qubit[numberOfQubits]) {
        Controlled X (Rest(qubits), Head(qubits));
    } 
}
```

## <a name="using-width-counter-within-a-c-program"></a><span data-ttu-id="6bb65-109">Verwenden des Width-Zählers innerhalb eines C# Programms</span><span class="sxs-lookup"><span data-stu-id="6bb65-109">Using Width Counter within a C# Program</span></span>

<span data-ttu-id="6bb65-110">Bei der multiplizierten `X`, die auf insgesamt 5 Qubits wirkt, werden zwei hilfskbits und die Eingabe Breite 5 verwendet.</span><span class="sxs-lookup"><span data-stu-id="6bb65-110">Multiply controlled `X` acting on a total of 5 qubits will allocate 2 ancillary qubits and its input width will be 5.</span></span> <span data-ttu-id="6bb65-111">Um zu überprüfen, ob dies der Fall ist, können wir C# Folgendes Programm verwenden:</span><span class="sxs-lookup"><span data-stu-id="6bb65-111">To check that this is the case, we can use the following C# program:</span></span>

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

<span data-ttu-id="6bb65-112">Der erste Teil des Programms führt `ApplyMultiControlledX`aus.</span><span class="sxs-lookup"><span data-stu-id="6bb65-112">The first part of the program executes `ApplyMultiControlledX`.</span></span> <span data-ttu-id="6bb65-113">Im zweiten Teil verwenden wir die-Methode `QCTraceSimulator.GetMetric`, um die Anzahl der zugeordneten Qubits abzurufen, sowie die Anzahl der Qubits, die `X` als Eingabe empfangen haben.</span><span class="sxs-lookup"><span data-stu-id="6bb65-113">In the second part we use the method `QCTraceSimulator.GetMetric` to get the number of allocated qubits as well as the number of qubits that Controlled `X` received as input.</span></span> 

<span data-ttu-id="6bb65-114">Zum Schluss können Sie die folgenden Informationen verwenden, um alle Statistiken auszugeben, die von der Width-Zahl im CSV-Format erfasst wurden:</span><span class="sxs-lookup"><span data-stu-id="6bb65-114">Finally, to output all the statistics collected by width counter in CSV format we can use the following:</span></span>
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.widthCounter];
```

## <a name="see-also"></a><span data-ttu-id="6bb65-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6bb65-115">See also</span></span> ##

- <span data-ttu-id="6bb65-116">Übersicht über den Ablauf [Verfolgungs Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) für Quantum-Computer</span><span class="sxs-lookup"><span data-stu-id="6bb65-116">The quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>

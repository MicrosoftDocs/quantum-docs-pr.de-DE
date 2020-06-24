---
title: Breiten-Counter
description: Erfahren Sie mehr über den Microsoft QDK Width-Zähler, der die Anzahl der von jedem Vorgang in einem Quantum-Programm zugeordneten und zugeordneten Qubits zählt.
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.width-counter
ms.openlocfilehash: a76292222950310acc90dded02980e4a5b792e76
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274896"
---
# <a name="width-counter"></a><span data-ttu-id="c2116-103">Breiten-Counter</span><span class="sxs-lookup"><span data-stu-id="c2116-103">Width Counter</span></span>

<span data-ttu-id="c2116-104">Der `Width Counter` zählt die Anzahl der von jedem Vorgang zugeordneten und zugeordneten Qubits.</span><span class="sxs-lookup"><span data-stu-id="c2116-104">The `Width Counter` counts the number of qubits allocated and borrowed by each operation.</span></span>
<span data-ttu-id="c2116-105">Alle Vorgänge aus dem- `Microsoft.Quantum.Intrinsic` Namespace werden in Form einzelner Qubit-Drehungen, T Gates, einzelner Qubit Clifford Gates, CNOT Gates und Messungen von Multi-Qubit Pauli Observables ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="c2116-105">All operations from the `Microsoft.Quantum.Intrinsic` namespace are expressed in terms of single qubit rotations, T gates, single qubit Clifford gates, CNOT gates and measurements of multi-qubit Pauli observables.</span></span> <span data-ttu-id="c2116-106">Einige der primitiven Vorgänge können zusätzliche Qubits zuordnen.</span><span class="sxs-lookup"><span data-stu-id="c2116-106">Some of the primitive operations can allocate extra qubits.</span></span> <span data-ttu-id="c2116-107">Multiplizieren Sie z `X` . b. gesteuerte Gates oder kontrollierte `T` Gates.</span><span class="sxs-lookup"><span data-stu-id="c2116-107">For example, multiply controlled `X` gates or controlled `T` gates.</span></span> <span data-ttu-id="c2116-108">Wir berechnen die Anzahl zusätzlicher Qubits, die durch die Implementierung eines mehrfach gesteuerten Tors zugeordnet werden `X` :</span><span class="sxs-lookup"><span data-stu-id="c2116-108">Let us compute the number of extra qubits allocated by the implementation of a multiply controlled `X` gate:</span></span>

```qsharp
open Microsoft.Quantum.Intrinsic;
open Microsoft.Quantum.Arrays;
operation ApplyMultiControlledX( numberOfQubits : Int ) : Unit {
    using(qubits = Qubit[numberOfQubits]) {
        Controlled X (Rest(qubits), Head(qubits));
    } 
}
```

## <a name="using-width-counter-within-a-c-program"></a><span data-ttu-id="c2116-109">Verwenden des Width-Zählers innerhalb eines c#-Programms</span><span class="sxs-lookup"><span data-stu-id="c2116-109">Using Width Counter within a C# Program</span></span>

<span data-ttu-id="c2116-110">Die Multiplikation, `X` die auf insgesamt 5 Qubits durchführt, weist 2 hilfskbits zu, und die Eingabe Breite ist 5.</span><span class="sxs-lookup"><span data-stu-id="c2116-110">Multiply controlled `X` acting on a total of 5 qubits will allocate 2 ancillary qubits and its input width will be 5.</span></span> <span data-ttu-id="c2116-111">Um zu überprüfen, ob dies der Fall ist, können wir das folgende c#-Programm verwenden:</span><span class="sxs-lookup"><span data-stu-id="c2116-111">To check that this is the case, we can use the following C# program:</span></span>

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

<span data-ttu-id="c2116-112">Der erste Teil des Programms wird ausgeführt `ApplyMultiControlledX` .</span><span class="sxs-lookup"><span data-stu-id="c2116-112">The first part of the program executes `ApplyMultiControlledX`.</span></span> <span data-ttu-id="c2116-113">Im zweiten Teil wird die-Methode verwendet `QCTraceSimulator.GetMetric` , um die Anzahl der zugeordneten Qubits sowie die Anzahl von Qubits abzurufen, die von `X` als Eingabe gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="c2116-113">In the second part we use the method `QCTraceSimulator.GetMetric` to get the number of allocated qubits as well as the number of qubits that Controlled `X` received as input.</span></span> 

<span data-ttu-id="c2116-114">Zum Schluss können Sie die folgenden Informationen verwenden, um alle Statistiken auszugeben, die von der Width-Zahl im CSV-Format erfasst wurden:</span><span class="sxs-lookup"><span data-stu-id="c2116-114">Finally, to output all the statistics collected by width counter in CSV format we can use the following:</span></span>
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.widthCounter];
```

## <a name="see-also"></a><span data-ttu-id="c2116-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c2116-115">See also</span></span> ##

- <span data-ttu-id="c2116-116">Übersicht über den Ablauf [Verfolgungs Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) für Quantum-Computer</span><span class="sxs-lookup"><span data-stu-id="c2116-116">The quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>

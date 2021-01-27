---
uid: Microsoft.Quantum.Simulation.TimeDependentTrotterSimulationAlgorithmImpl
title: Timedependenttrottersimulationalgorithmimpl-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TimeDependentTrotterSimulationAlgorithmImpl
qsharp.summary: Implementation of multiple Trotter steps to approximate a unitary operator that solves the time-dependent Schrödinger equation.
ms.openlocfilehash: 3a23c14e8181eeaf1614dab6f8aa5a002364c2b8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847803"
---
# <a name="timedependenttrottersimulationalgorithmimpl-operation"></a><span data-ttu-id="5fc4b-102">Timedependenttrottersimulationalgorithmimpl-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5fc4b-102">TimeDependentTrotterSimulationAlgorithmImpl operation</span></span>

<span data-ttu-id="5fc4b-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="5fc4b-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="5fc4b-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5fc4b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5fc4b-105">Implementierung mehrerer trockschritte zur Annäherung an einen einheitlichen Operator, der die zeitabhängige Schrödinger-Gleichung löst.</span><span class="sxs-lookup"><span data-stu-id="5fc4b-105">Implementation of multiple Trotter steps to approximate a unitary operator that solves the time-dependent Schrödinger equation.</span></span>

```qsharp
operation TimeDependentTrotterSimulationAlgorithmImpl (trotterStepSize : Double, trotterOrder : Int, maxTime : Double, evolutionSchedule : Microsoft.Quantum.Simulation.EvolutionSchedule, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="5fc4b-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5fc4b-106">Input</span></span>

### <a name="trotterstepsize--double"></a><span data-ttu-id="5fc4b-107">trotterstepsize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="5fc4b-107">trotterStepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="5fc4b-108">Dauer der simulierten Zeitentwicklung in einem einzelnen trockschritt.</span><span class="sxs-lookup"><span data-stu-id="5fc4b-108">Duration of simulated time-evolution in single Trotter step.</span></span>


### <a name="trotterorder--int"></a><span data-ttu-id="5fc4b-109">trotterorder: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5fc4b-109">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5fc4b-110">Reihenfolge des trockintegrator.</span><span class="sxs-lookup"><span data-stu-id="5fc4b-110">Order of Trotter integrator.</span></span> <span data-ttu-id="5fc4b-111">Dies muss entweder 1 oder eine gerade Zahl sein.</span><span class="sxs-lookup"><span data-stu-id="5fc4b-111">This must be either 1 or an even number.</span></span>


### <a name="maxtime--double"></a><span data-ttu-id="5fc4b-112">maxTime: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="5fc4b-112">maxTime : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="5fc4b-113">Gesamtdauer der Simulation $t $.</span><span class="sxs-lookup"><span data-stu-id="5fc4b-113">Total duration of simulation $t$.</span></span>


### <a name="evolutionschedule--evolutionschedule"></a><span data-ttu-id="5fc4b-114">evolutionschedule: [evolutionschedule](xref:Microsoft.Quantum.Simulation.EvolutionSchedule)</span><span class="sxs-lookup"><span data-stu-id="5fc4b-114">evolutionSchedule : [EvolutionSchedule](xref:Microsoft.Quantum.Simulation.EvolutionSchedule)</span></span>

<span data-ttu-id="5fc4b-115">Eine umfassende Beschreibung des zeitabhängigen Systems, das simuliert werden soll.</span><span class="sxs-lookup"><span data-stu-id="5fc4b-115">A complete description of the time-dependent system to be simulated.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="5fc4b-116">Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="5fc4b-116">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="5fc4b-117">Die von der Simulation abgewickelten Qubits.</span><span class="sxs-lookup"><span data-stu-id="5fc4b-117">Qubits acted on by simulation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5fc4b-118">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5fc4b-118">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>


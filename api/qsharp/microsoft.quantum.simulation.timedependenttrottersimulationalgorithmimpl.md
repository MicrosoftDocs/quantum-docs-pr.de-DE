---
uid: Microsoft.Quantum.Simulation.TimeDependentTrotterSimulationAlgorithmImpl
title: Timedependenttrottersimulationalgorithmimpl-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TimeDependentTrotterSimulationAlgorithmImpl
qsharp.summary: Implementation of multiple Trotter steps to approximate a unitary operator that solves the time-dependent Schrödinger equation.
ms.openlocfilehash: c6d1c976d29c69d3ac14d9a2be09826602c8cc1d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706434"
---
# <a name="timedependenttrottersimulationalgorithmimpl-operation"></a><span data-ttu-id="eef92-102">Timedependenttrottersimulationalgorithmimpl-Vorgang</span><span class="sxs-lookup"><span data-stu-id="eef92-102">TimeDependentTrotterSimulationAlgorithmImpl operation</span></span>

<span data-ttu-id="eef92-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="eef92-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="eef92-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="eef92-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="eef92-105">Implementierung mehrerer trockschritte zur Annäherung an einen einheitlichen Operator, der die zeitabhängige Schrödinger-Gleichung löst.</span><span class="sxs-lookup"><span data-stu-id="eef92-105">Implementation of multiple Trotter steps to approximate a unitary operator that solves the time-dependent Schrödinger equation.</span></span>

```qsharp
operation TimeDependentTrotterSimulationAlgorithmImpl (trotterStepSize : Double, trotterOrder : Int, maxTime : Double, evolutionSchedule : Microsoft.Quantum.Simulation.EvolutionSchedule, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="eef92-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="eef92-106">Input</span></span>

### <a name="trotterstepsize--double"></a><span data-ttu-id="eef92-107">trotterstepsize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="eef92-107">trotterStepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="eef92-108">Dauer der simulierten Zeitentwicklung in einem einzelnen trockschritt.</span><span class="sxs-lookup"><span data-stu-id="eef92-108">Duration of simulated time-evolution in single Trotter step.</span></span>


### <a name="trotterorder--int"></a><span data-ttu-id="eef92-109">trotterorder: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="eef92-109">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="eef92-110">Reihenfolge des trockintegrator.</span><span class="sxs-lookup"><span data-stu-id="eef92-110">Order of Trotter integrator.</span></span> <span data-ttu-id="eef92-111">Dies muss entweder 1 oder eine gerade Zahl sein.</span><span class="sxs-lookup"><span data-stu-id="eef92-111">This must be either 1 or an even number.</span></span>


### <a name="maxtime--double"></a><span data-ttu-id="eef92-112">maxTime: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="eef92-112">maxTime : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="eef92-113">Gesamtdauer der Simulation $t $.</span><span class="sxs-lookup"><span data-stu-id="eef92-113">Total duration of simulation $t$.</span></span>


### <a name="evolutionschedule--evolutionschedule"></a><span data-ttu-id="eef92-114">evolutionschedule: [evolutionschedule](xref:Microsoft.Quantum.Simulation.EvolutionSchedule)</span><span class="sxs-lookup"><span data-stu-id="eef92-114">evolutionSchedule : [EvolutionSchedule](xref:Microsoft.Quantum.Simulation.EvolutionSchedule)</span></span>

<span data-ttu-id="eef92-115">Eine umfassende Beschreibung des zeitabhängigen Systems, das simuliert werden soll.</span><span class="sxs-lookup"><span data-stu-id="eef92-115">A complete description of the time-dependent system to be simulated.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="eef92-116">Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="eef92-116">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="eef92-117">Die von der Simulation abgewickelten Qubits.</span><span class="sxs-lookup"><span data-stu-id="eef92-117">Qubits acted on by simulation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="eef92-118">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="eef92-118">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>


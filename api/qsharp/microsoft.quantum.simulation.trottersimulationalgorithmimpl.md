---
uid: Microsoft.Quantum.Simulation.TrotterSimulationAlgorithmImpl
title: Trottersimulationalgorithmimpl-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TrotterSimulationAlgorithmImpl
qsharp.summary: Makes repeated calls to `TrotterStep` to approximate the time-evolution operator exp(_-iHt_).
ms.openlocfilehash: 5b796245e2a4434228260a229cb61be66f3e38d6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203398"
---
# <a name="trottersimulationalgorithmimpl-operation"></a><span data-ttu-id="7dca6-102">Trottersimulationalgorithmimpl-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7dca6-102">TrotterSimulationAlgorithmImpl operation</span></span>

<span data-ttu-id="7dca6-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="7dca6-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="7dca6-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7dca6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7dca6-105">Führt wiederkehrende Aufrufe von aus `TrotterStep` , um den Zeit-Evolution-Operator Exp (_-IHT_) zu nähern.</span><span class="sxs-lookup"><span data-stu-id="7dca6-105">Makes repeated calls to `TrotterStep` to approximate the time-evolution operator exp(_-iHt_).</span></span>

```qsharp
operation TrotterSimulationAlgorithmImpl (trotterStepSize : Double, trotterOrder : Int, maxTime : Double, evolutionGenerator : Microsoft.Quantum.Simulation.EvolutionGenerator, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="7dca6-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7dca6-106">Input</span></span>

### <a name="trotterstepsize--double"></a><span data-ttu-id="7dca6-107">trotterstepsize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="7dca6-107">trotterStepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="7dca6-108">Dauer der simulierten Zeitentwicklung in einem einzelnen trockschritt.</span><span class="sxs-lookup"><span data-stu-id="7dca6-108">Duration of simulated time-evolution in single Trotter step.</span></span>


### <a name="trotterorder--int"></a><span data-ttu-id="7dca6-109">trotterorder: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7dca6-109">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="7dca6-110">Reihenfolge des trockintegrator.</span><span class="sxs-lookup"><span data-stu-id="7dca6-110">Order of Trotter integrator.</span></span> <span data-ttu-id="7dca6-111">Dies muss entweder 1 oder eine gerade Zahl sein.</span><span class="sxs-lookup"><span data-stu-id="7dca6-111">This must be either 1 or an even number.</span></span>


### <a name="maxtime--double"></a><span data-ttu-id="7dca6-112">maxTime: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="7dca6-112">maxTime : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="7dca6-113">Gesamtdauer der Simulation $t $.</span><span class="sxs-lookup"><span data-stu-id="7dca6-113">Total duration of simulation $t$.</span></span>


### <a name="evolutiongenerator--evolutiongenerator"></a><span data-ttu-id="7dca6-114">evolutiongenerator: [evolutiongenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span><span class="sxs-lookup"><span data-stu-id="7dca6-114">evolutionGenerator : [EvolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span></span>

<span data-ttu-id="7dca6-115">Eine umfassende Beschreibung des Systems, das simuliert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7dca6-115">A complete description of the system to be simulated.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="7dca6-116">Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="7dca6-116">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="7dca6-117">Die von der Simulation abgewickelten Qubits.</span><span class="sxs-lookup"><span data-stu-id="7dca6-117">Qubits acted on by simulation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7dca6-118">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7dca6-118">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>


---
uid: Microsoft.Quantum.Simulation.TrotterSimulationAlgorithm
title: Trottersimulationalgorithmus-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TrotterSimulationAlgorithm
qsharp.summary: '`SimulationAlgorithm` function that uses a Trotter–Suzuki decomposition to approximate the time-evolution operator _exp(-iHt)_.'
ms.openlocfilehash: aa8338ab359441765db72a12f84a3a51e5bee3ce
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192535"
---
# <a name="trottersimulationalgorithm-function"></a><span data-ttu-id="6d4b3-102">Trottersimulationalgorithmus-Funktion</span><span class="sxs-lookup"><span data-stu-id="6d4b3-102">TrotterSimulationAlgorithm function</span></span>

<span data-ttu-id="6d4b3-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="6d4b3-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="6d4b3-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6d4b3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6d4b3-105">`SimulationAlgorithm` eine Funktion, die eine Trotter – Suzuki-Zerlegung verwendet, um den Time-Evolution Operator _Exp (-IHT)_ zu annähern.</span><span class="sxs-lookup"><span data-stu-id="6d4b3-105">`SimulationAlgorithm` function that uses a Trotter–Suzuki decomposition to approximate the time-evolution operator _exp(-iHt)_.</span></span>

```qsharp
function TrotterSimulationAlgorithm (trotterStepSize : Double, trotterOrder : Int) : Microsoft.Quantum.Simulation.SimulationAlgorithm
```


## <a name="input"></a><span data-ttu-id="6d4b3-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6d4b3-106">Input</span></span>

### <a name="trotterstepsize--double"></a><span data-ttu-id="6d4b3-107">trotterstepsize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="6d4b3-107">trotterStepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="6d4b3-108">Dauer der simulierten Zeitentwicklung in einem einzelnen trockschritt.</span><span class="sxs-lookup"><span data-stu-id="6d4b3-108">Duration of simulated time-evolution in single Trotter step.</span></span>


### <a name="trotterorder--int"></a><span data-ttu-id="6d4b3-109">trotterorder: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6d4b3-109">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6d4b3-110">Reihenfolge des trockintegrator.</span><span class="sxs-lookup"><span data-stu-id="6d4b3-110">Order of Trotter integrator.</span></span> <span data-ttu-id="6d4b3-111">Dies muss entweder 1 oder eine gerade Zahl sein.</span><span class="sxs-lookup"><span data-stu-id="6d4b3-111">This must be either 1 or an even number.</span></span>



## <a name="output--simulationalgorithm"></a><span data-ttu-id="6d4b3-112">Ausgabe: [simulationalgorithmus](xref:Microsoft.Quantum.Simulation.SimulationAlgorithm)</span><span class="sxs-lookup"><span data-stu-id="6d4b3-112">Output : [SimulationAlgorithm](xref:Microsoft.Quantum.Simulation.SimulationAlgorithm)</span></span>

<span data-ttu-id="6d4b3-113">Ein `SimulationAlgorithm`-Typ.</span><span class="sxs-lookup"><span data-stu-id="6d4b3-113">A `SimulationAlgorithm` type.</span></span>
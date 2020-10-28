---
uid: Microsoft.Quantum.Simulation.TrotterSimulationAlgorithm
title: Trottersimulationalgorithmus-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TrotterSimulationAlgorithm
qsharp.summary: '`SimulationAlgorithm` function that uses a Trotter–Suzuki decomposition to approximate the time-evolution operator _exp(-iHt)_.'
ms.openlocfilehash: c52acf293e69c78e7a82b0cf5d94de52d0f5a293
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706439"
---
# <a name="trottersimulationalgorithm-function"></a><span data-ttu-id="21a89-102">Trottersimulationalgorithmus-Funktion</span><span class="sxs-lookup"><span data-stu-id="21a89-102">TrotterSimulationAlgorithm function</span></span>

<span data-ttu-id="21a89-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="21a89-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="21a89-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="21a89-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="21a89-105">`SimulationAlgorithm` eine Funktion, die eine Trotter – Suzuki-Zerlegung verwendet, um den Time-Evolution Operator _Exp (-IHT)_ zu annähern.</span><span class="sxs-lookup"><span data-stu-id="21a89-105">`SimulationAlgorithm` function that uses a Trotter–Suzuki decomposition to approximate the time-evolution operator _exp(-iHt)_ .</span></span>

```qsharp
function TrotterSimulationAlgorithm (trotterStepSize : Double, trotterOrder : Int) : Microsoft.Quantum.Simulation.SimulationAlgorithm
```


## <a name="input"></a><span data-ttu-id="21a89-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="21a89-106">Input</span></span>

### <a name="trotterstepsize--double"></a><span data-ttu-id="21a89-107">trotterstepsize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="21a89-107">trotterStepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="21a89-108">Dauer der simulierten Zeitentwicklung in einem einzelnen trockschritt.</span><span class="sxs-lookup"><span data-stu-id="21a89-108">Duration of simulated time-evolution in single Trotter step.</span></span>


### <a name="trotterorder--int"></a><span data-ttu-id="21a89-109">trotterorder: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="21a89-109">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="21a89-110">Reihenfolge des trockintegrator.</span><span class="sxs-lookup"><span data-stu-id="21a89-110">Order of Trotter integrator.</span></span> <span data-ttu-id="21a89-111">Dies muss entweder 1 oder eine gerade Zahl sein.</span><span class="sxs-lookup"><span data-stu-id="21a89-111">This must be either 1 or an even number.</span></span>



## <a name="output--simulationalgorithm"></a><span data-ttu-id="21a89-112">Ausgabe: [simulationalgorithmus](xref:Microsoft.Quantum.Simulation.SimulationAlgorithm)</span><span class="sxs-lookup"><span data-stu-id="21a89-112">Output : [SimulationAlgorithm](xref:Microsoft.Quantum.Simulation.SimulationAlgorithm)</span></span>

<span data-ttu-id="21a89-113">Ein `SimulationAlgorithm`-Typ.</span><span class="sxs-lookup"><span data-stu-id="21a89-113">A `SimulationAlgorithm` type.</span></span>
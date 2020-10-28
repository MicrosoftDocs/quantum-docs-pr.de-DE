---
uid: Microsoft.Quantum.Simulation.TimeDependentTrotterSimulationAlgorithm
title: Timedependenttrottersimulationalgorithmus-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TimeDependentTrotterSimulationAlgorithm
qsharp.summary: '`TimeDependentSimulationAlgorithm` function that uses a Trotter–Suzuki decomposition to approximate a unitary operator that solves the time-dependent Schrodinger equation.'
ms.openlocfilehash: 6129d768276b5c9d96a1b1ed9cd5a6a22d28e286
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706442"
---
# <a name="timedependenttrottersimulationalgorithm-function"></a><span data-ttu-id="c377e-102">Timedependenttrottersimulationalgorithmus-Funktion</span><span class="sxs-lookup"><span data-stu-id="c377e-102">TimeDependentTrotterSimulationAlgorithm function</span></span>

<span data-ttu-id="c377e-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="c377e-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="c377e-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c377e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c377e-105">`TimeDependentSimulationAlgorithm` eine Funktion, die eine Trotter – Suzuki-Zerlegung verwendet, um einen einheitlichen Operator zu nähern, der die zeitabhängige Schrodinger-Gleichung löst.</span><span class="sxs-lookup"><span data-stu-id="c377e-105">`TimeDependentSimulationAlgorithm` function that uses a Trotter–Suzuki decomposition to approximate a unitary operator that solves the time-dependent Schrodinger equation.</span></span>

```qsharp
function TimeDependentTrotterSimulationAlgorithm (trotterStepSize : Double, trotterOrder : Int) : Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm
```


## <a name="input"></a><span data-ttu-id="c377e-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c377e-106">Input</span></span>

### <a name="trotterstepsize--double"></a><span data-ttu-id="c377e-107">trotterstepsize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="c377e-107">trotterStepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="c377e-108">Dauer der simulierten Zeitentwicklung in einem einzelnen trockschritt.</span><span class="sxs-lookup"><span data-stu-id="c377e-108">Duration of simulated time-evolution in single Trotter step.</span></span>


### <a name="trotterorder--int"></a><span data-ttu-id="c377e-109">trotterorder: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c377e-109">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c377e-110">Reihenfolge des trockintegrator.</span><span class="sxs-lookup"><span data-stu-id="c377e-110">Order of Trotter integrator.</span></span> <span data-ttu-id="c377e-111">Dies muss entweder 1 oder eine gerade Zahl sein.</span><span class="sxs-lookup"><span data-stu-id="c377e-111">This must be either 1 or an even number.</span></span>



## <a name="output--timedependentsimulationalgorithm"></a><span data-ttu-id="c377e-112">Ausgabe: [timedependentsimulationalgorithmus](xref:Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm)</span><span class="sxs-lookup"><span data-stu-id="c377e-112">Output : [TimeDependentSimulationAlgorithm](xref:Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm)</span></span>

<span data-ttu-id="c377e-113">Ein `TimeDependentSimulationAlgorithm`-Typ.</span><span class="sxs-lookup"><span data-stu-id="c377e-113">A `TimeDependentSimulationAlgorithm` type.</span></span>
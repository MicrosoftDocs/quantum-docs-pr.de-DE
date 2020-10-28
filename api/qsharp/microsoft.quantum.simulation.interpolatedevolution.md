---
uid: Microsoft.Quantum.Simulation.InterpolatedEvolution
title: Interpolatedevolution-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: InterpolatedEvolution
qsharp.summary: Interpolates between two generators with a uniform schedule, returning an operation that applies simulated evolution under the resulting time-dependent generator to a qubit register.
ms.openlocfilehash: 18026b9872f6a3344a1e5c2122f55927975ccb59
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701730"
---
# <a name="interpolatedevolution-function"></a><span data-ttu-id="d7c1b-102">Interpolatedevolution-Funktion</span><span class="sxs-lookup"><span data-stu-id="d7c1b-102">InterpolatedEvolution function</span></span>

<span data-ttu-id="d7c1b-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="d7c1b-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="d7c1b-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d7c1b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d7c1b-105">Interpoliert zwischen zwei Generatoren mit einem einheitlichen Zeitplan und gibt einen Vorgang zurück, der die simulierte Weiterentwicklung unter dem resultierenden zeitabhängigen Generator auf ein Qubit-Register anwendet.</span><span class="sxs-lookup"><span data-stu-id="d7c1b-105">Interpolates between two generators with a uniform schedule, returning an operation that applies simulated evolution under the resulting time-dependent generator to a qubit register.</span></span>

```qsharp
function InterpolatedEvolution (interpolationTime : Double, evolutionGeneratorStart : Microsoft.Quantum.Simulation.EvolutionGenerator, evolutionGeneratorEnd : Microsoft.Quantum.Simulation.EvolutionGenerator, timeDependentSimulationAlgorithm : Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="d7c1b-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d7c1b-106">Input</span></span>

### <a name="interpolationtime--double"></a><span data-ttu-id="d7c1b-107">interpolationtime: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="d7c1b-107">interpolationTime : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="d7c1b-108">Zeit zum Ausführen der Interpolations Zeit.</span><span class="sxs-lookup"><span data-stu-id="d7c1b-108">Time to perform the interpolation over.</span></span>


### <a name="evolutiongeneratorstart--evolutiongenerator"></a><span data-ttu-id="d7c1b-109">evolutiongeneratorstart: [evolutiongenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span><span class="sxs-lookup"><span data-stu-id="d7c1b-109">evolutionGeneratorStart : [EvolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span></span>

<span data-ttu-id="d7c1b-110">Ursprünglicher Generator, unter dem die Entwicklung simuliert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d7c1b-110">Initial generator to simulate evolution under.</span></span>


### <a name="evolutiongeneratorend--evolutiongenerator"></a><span data-ttu-id="d7c1b-111">evolutiongeneratorend: [evolutiongenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span><span class="sxs-lookup"><span data-stu-id="d7c1b-111">evolutionGeneratorEnd : [EvolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span></span>

<span data-ttu-id="d7c1b-112">Der endgültige Generator, unter dem die Entwicklung simuliert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d7c1b-112">Final generator to simulate evolution under.</span></span>


### <a name="timedependentsimulationalgorithm--timedependentsimulationalgorithm"></a><span data-ttu-id="d7c1b-113">timedependentsimulationalgorithmus: [timedependentsimulationalgorithmus](xref:Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm)</span><span class="sxs-lookup"><span data-stu-id="d7c1b-113">timeDependentSimulationAlgorithm : [TimeDependentSimulationAlgorithm](xref:Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm)</span></span>

<span data-ttu-id="d7c1b-114">Ein zeitabhängiger Simulations Algorithmus, der verwendet wird, um die Evolution während des einheitlichen Interpolations Zeitplans zu simulieren.</span><span class="sxs-lookup"><span data-stu-id="d7c1b-114">A time-dependent simulation algorithm that will be used to simulate evolution during the uniform interpolation schedule.</span></span>



## <a name="output--qubit--unit-adj--ctl"></a><span data-ttu-id="d7c1b-115">Ausgabe: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="d7c1b-115">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>



## <a name="remarks"></a><span data-ttu-id="d7c1b-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d7c1b-116">Remarks</span></span>

<span data-ttu-id="d7c1b-117">Wenn die Interpolations Zeit ausgewählt ist, um die adiabatischen Bedingungen zu erfüllen, gibt diese Funktion einen Vorgang zurück, der die adiabatische Zustands Vorbereitung für den endgültigen Dynamical-Generator ausführt.</span><span class="sxs-lookup"><span data-stu-id="d7c1b-117">If the interpolation time is chosen to meet the adiabatic conditions, then this function returns an operation which performs adiabatic state preparation for the final dynamical generator.</span></span>
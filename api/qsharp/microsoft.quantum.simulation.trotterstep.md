---
uid: Microsoft.Quantum.Simulation.TrotterStep
title: Trotterstep-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TrotterStep
qsharp.summary: Implements a single time-step of time-evolution by the system described in an `EvolutionGenerator` using a Trotter–Suzuki decomposition.
ms.openlocfilehash: 7a1a27ba4dc4b8b7bbc4da6a378d4a1494bc9415
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725355"
---
# <a name="trotterstep-function"></a><span data-ttu-id="141d0-102">Trotterstep-Funktion</span><span class="sxs-lookup"><span data-stu-id="141d0-102">TrotterStep function</span></span>

<span data-ttu-id="141d0-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="141d0-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="141d0-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="141d0-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="141d0-105">Implementiert einen einzelnen Zeit Schritt der Zeitentwicklung durch das in einer `EvolutionGenerator` mithilfe einer Trotter – Suzuki-Zerlegung beschriebene System.</span><span class="sxs-lookup"><span data-stu-id="141d0-105">Implements a single time-step of time-evolution by the system described in an `EvolutionGenerator` using a Trotter–Suzuki decomposition.</span></span>

```qsharp
function TrotterStep (evolutionGenerator : Microsoft.Quantum.Simulation.EvolutionGenerator, trotterOrder : Int, trotterStepSize : Double) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="141d0-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="141d0-106">Input</span></span>

### <a name="evolutiongenerator--evolutiongenerator"></a><span data-ttu-id="141d0-107">evolutiongenerator: [evolutiongenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span><span class="sxs-lookup"><span data-stu-id="141d0-107">evolutionGenerator : [EvolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span></span>

<span data-ttu-id="141d0-108">Eine umfassende Beschreibung des Systems, das simuliert werden soll.</span><span class="sxs-lookup"><span data-stu-id="141d0-108">A complete description of the system to be simulated.</span></span>


### <a name="trotterorder--int"></a><span data-ttu-id="141d0-109">trotterorder: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="141d0-109">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="141d0-110">Reihenfolge des trockintegrator.</span><span class="sxs-lookup"><span data-stu-id="141d0-110">Order of Trotter integrator.</span></span> <span data-ttu-id="141d0-111">Dies muss entweder 1 oder eine gerade Zahl sein.</span><span class="sxs-lookup"><span data-stu-id="141d0-111">This must be either 1 or an even number.</span></span>


### <a name="trotterstepsize--double"></a><span data-ttu-id="141d0-112">trotterstepsize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="141d0-112">trotterStepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="141d0-113">Dauer der simulierten Zeitentwicklung in einem einzelnen trockschritt.</span><span class="sxs-lookup"><span data-stu-id="141d0-113">Duration of simulated time-evolution in single Trotter step.</span></span>



## <a name="output--qubit--unit-adj--ctl"></a><span data-ttu-id="141d0-114">Ausgabe: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="141d0-114">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="141d0-115">Einheitlicher Vorgang, der einen einzelnen Schritt der Zeit-Evolution für die Dauer angleicht `trotterStepSize` .</span><span class="sxs-lookup"><span data-stu-id="141d0-115">Unitary operation that approximates a single step of time-evolution for duration `trotterStepSize`.</span></span>

## <a name="remarks"></a><span data-ttu-id="141d0-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="141d0-116">Remarks</span></span>

<span data-ttu-id="141d0-117">Weitere Informationen zur Trotter – Suzuki-Zerlegung finden Sie unter [Zeit geordnete Komposition](/quantum/libraries/control-flow#time-ordered-composition).</span><span class="sxs-lookup"><span data-stu-id="141d0-117">For more on the Trotter–Suzuki decomposition, see [Time-Ordered Composition](/quantum/libraries/control-flow#time-ordered-composition).</span></span>
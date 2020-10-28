---
uid: Microsoft.Quantum.Simulation.InterpolateGeneratorSystems
title: Interpolategeneratorsystems-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: InterpolateGeneratorSystems
qsharp.summary: Returns a `TimeDependentGeneratorSystem` representing the linear interpolation between two `GeneratorSystem`s.
ms.openlocfilehash: 9881c27577023dafff0bfc6d961877db44fec0eb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701723"
---
# <a name="interpolategeneratorsystems-function"></a><span data-ttu-id="59b41-102">Interpolategeneratorsystems-Funktion</span><span class="sxs-lookup"><span data-stu-id="59b41-102">InterpolateGeneratorSystems function</span></span>

<span data-ttu-id="59b41-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="59b41-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="59b41-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="59b41-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="59b41-105">Gibt einen zurück, `TimeDependentGeneratorSystem` der die lineare interpolung zwischen zwei `GeneratorSystem` n darstellt.</span><span class="sxs-lookup"><span data-stu-id="59b41-105">Returns a `TimeDependentGeneratorSystem` representing the linear interpolation between two `GeneratorSystem`s.</span></span>

```qsharp
function InterpolateGeneratorSystems (generatorSystemStart : Microsoft.Quantum.Simulation.GeneratorSystem, generatorSystemEnd : Microsoft.Quantum.Simulation.GeneratorSystem) : Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem
```


## <a name="input"></a><span data-ttu-id="59b41-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="59b41-106">Input</span></span>

### <a name="generatorsystemstart--generatorsystem"></a><span data-ttu-id="59b41-107">generatorsystemstart: [Generatorsystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="59b41-107">generatorSystemStart : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="59b41-108">Der Start `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="59b41-108">The start `GeneratorSystem`.</span></span>


### <a name="generatorsystemend--generatorsystem"></a><span data-ttu-id="59b41-109">generatorsystemend: [Generatorsystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="59b41-109">generatorSystemEnd : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="59b41-110">Das Ende `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="59b41-110">The end `GeneratorSystem`.</span></span>



## <a name="output--timedependentgeneratorsystem"></a><span data-ttu-id="59b41-111">Ausgabe: [timedependentgeneratorsystem](xref:Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="59b41-111">Output : [TimeDependentGeneratorSystem](xref:Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem)</span></span>

<span data-ttu-id="59b41-112">Ein `TimeDependentGeneratorSystem` , das ein System darstellt, das die Summe der Eingabe Generator Systeme ist, mit der Gewichtung $ (1-s) $ on `generatorSystemStart` und Weight $s $ on `generatorSystemEnd` .</span><span class="sxs-lookup"><span data-stu-id="59b41-112">A `TimeDependentGeneratorSystem` representing a system that is the sum of the input generator systems, with weight $(1-s)$ on `generatorSystemStart` and weight $s$ on `generatorSystemEnd`.</span></span>

## <a name="see-also"></a><span data-ttu-id="59b41-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="59b41-113">See Also</span></span>

- [<span data-ttu-id="59b41-114">Microsoft. Quantum. Simulation. Generatorsystem</span><span class="sxs-lookup"><span data-stu-id="59b41-114">Microsoft.Quantum.Simulation.GeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorSystem)
- [<span data-ttu-id="59b41-115">Microsoft. Quantum. Simulation. timedependentgeneratorsystem</span><span class="sxs-lookup"><span data-stu-id="59b41-115">Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem)
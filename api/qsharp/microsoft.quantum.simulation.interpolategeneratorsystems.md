---
uid: Microsoft.Quantum.Simulation.InterpolateGeneratorSystems
title: Interpolategeneratorsystems-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: InterpolateGeneratorSystems
qsharp.summary: Returns a `TimeDependentGeneratorSystem` representing the linear interpolation between two `GeneratorSystem`s.
ms.openlocfilehash: ee47637996313fe1b77c76f00b08417dac956247
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230581"
---
# <a name="interpolategeneratorsystems-function"></a><span data-ttu-id="740e6-102">Interpolategeneratorsystems-Funktion</span><span class="sxs-lookup"><span data-stu-id="740e6-102">InterpolateGeneratorSystems function</span></span>

<span data-ttu-id="740e6-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="740e6-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="740e6-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="740e6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="740e6-105">Gibt einen zurück, `TimeDependentGeneratorSystem` der die lineare interpolung zwischen zwei `GeneratorSystem` n darstellt.</span><span class="sxs-lookup"><span data-stu-id="740e6-105">Returns a `TimeDependentGeneratorSystem` representing the linear interpolation between two `GeneratorSystem`s.</span></span>

```qsharp
function InterpolateGeneratorSystems (generatorSystemStart : Microsoft.Quantum.Simulation.GeneratorSystem, generatorSystemEnd : Microsoft.Quantum.Simulation.GeneratorSystem) : Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem
```


## <a name="input"></a><span data-ttu-id="740e6-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="740e6-106">Input</span></span>

### <a name="generatorsystemstart--generatorsystem"></a><span data-ttu-id="740e6-107">generatorsystemstart: [Generatorsystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="740e6-107">generatorSystemStart : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="740e6-108">Der Start `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="740e6-108">The start `GeneratorSystem`.</span></span>


### <a name="generatorsystemend--generatorsystem"></a><span data-ttu-id="740e6-109">generatorsystemend: [Generatorsystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="740e6-109">generatorSystemEnd : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="740e6-110">Das Ende `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="740e6-110">The end `GeneratorSystem`.</span></span>



## <a name="output--timedependentgeneratorsystem"></a><span data-ttu-id="740e6-111">Ausgabe: [timedependentgeneratorsystem](xref:Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="740e6-111">Output : [TimeDependentGeneratorSystem](xref:Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem)</span></span>

<span data-ttu-id="740e6-112">Ein `TimeDependentGeneratorSystem` , das ein System darstellt, das die Summe der Eingabe Generator Systeme ist, mit der Gewichtung $ (1-s) $ on `generatorSystemStart` und Weight $s $ on `generatorSystemEnd` .</span><span class="sxs-lookup"><span data-stu-id="740e6-112">A `TimeDependentGeneratorSystem` representing a system that is the sum of the input generator systems, with weight $(1-s)$ on `generatorSystemStart` and weight $s$ on `generatorSystemEnd`.</span></span>

## <a name="see-also"></a><span data-ttu-id="740e6-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="740e6-113">See Also</span></span>

- [<span data-ttu-id="740e6-114">Microsoft. Quantum. Simulation. Generatorsystem</span><span class="sxs-lookup"><span data-stu-id="740e6-114">Microsoft.Quantum.Simulation.GeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorSystem)
- [<span data-ttu-id="740e6-115">Microsoft. Quantum. Simulation. timedependentgeneratorsystem</span><span class="sxs-lookup"><span data-stu-id="740e6-115">Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem)
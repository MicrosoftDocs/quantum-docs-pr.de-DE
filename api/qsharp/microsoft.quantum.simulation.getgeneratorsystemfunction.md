---
uid: Microsoft.Quantum.Simulation.GetGeneratorSystemFunction
title: Getgeneratorsystemfunction-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: GetGeneratorSystemFunction
qsharp.summary: Retrieves the `GeneratorIndex` function in a `GeneratorSystem`.
ms.openlocfilehash: 60ebbdbd1020d41a54426377043fc0c84ceec504
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724557"
---
# <a name="getgeneratorsystemfunction-function"></a><span data-ttu-id="0f8f5-102">Getgeneratorsystemfunction-Funktion</span><span class="sxs-lookup"><span data-stu-id="0f8f5-102">GetGeneratorSystemFunction function</span></span>

<span data-ttu-id="0f8f5-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="0f8f5-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="0f8f5-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0f8f5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0f8f5-105">Ruft die- `GeneratorIndex` Funktion in einem ab `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="0f8f5-105">Retrieves the `GeneratorIndex` function in a `GeneratorSystem`.</span></span>

```qsharp
function GetGeneratorSystemFunction (generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem) : (Int -> Microsoft.Quantum.Simulation.GeneratorIndex)
```


## <a name="input"></a><span data-ttu-id="0f8f5-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0f8f5-106">Input</span></span>

### <a name="generatorsystem--generatorsystem"></a><span data-ttu-id="0f8f5-107">Generatorsystem: [Generatorsystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="0f8f5-107">generatorSystem : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="0f8f5-108">Die gewünschte `GeneratorSystem`.</span><span class="sxs-lookup"><span data-stu-id="0f8f5-108">The `GeneratorSystem` of interest.</span></span>



## <a name="output--int---generatorindex"></a><span data-ttu-id="0f8f5-109">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int) -> [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="0f8f5-109">Output : [Int](xref:microsoft.quantum.lang-ref.int) -> [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="0f8f5-110">Eine Funktion, die jeden `GeneratorIndex` Begriff in einer hamiltonan indiziert.</span><span class="sxs-lookup"><span data-stu-id="0f8f5-110">An function that indexes each `GeneratorIndex` term in a Hamiltonian.</span></span>

## <a name="see-also"></a><span data-ttu-id="0f8f5-111">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0f8f5-111">See Also</span></span>

- [<span data-ttu-id="0f8f5-112">Microsoft. Quantum. Simulation. generatorindex</span><span class="sxs-lookup"><span data-stu-id="0f8f5-112">Microsoft.Quantum.Simulation.GeneratorIndex</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorIndex)
- [<span data-ttu-id="0f8f5-113">Microsoft. Quantum. Simulation. Generatorsystem</span><span class="sxs-lookup"><span data-stu-id="0f8f5-113">Microsoft.Quantum.Simulation.GeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorSystem)
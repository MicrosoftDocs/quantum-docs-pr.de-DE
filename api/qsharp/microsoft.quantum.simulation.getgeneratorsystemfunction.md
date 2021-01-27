---
uid: Microsoft.Quantum.Simulation.GetGeneratorSystemFunction
title: Getgeneratorsystemfunction-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: GetGeneratorSystemFunction
qsharp.summary: Retrieves the `GeneratorIndex` function in a `GeneratorSystem`.
ms.openlocfilehash: 7b6eabd203cecf8c64f0bff3e06f08a0bec31bf2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852774"
---
# <a name="getgeneratorsystemfunction-function"></a><span data-ttu-id="e902a-102">Getgeneratorsystemfunction-Funktion</span><span class="sxs-lookup"><span data-stu-id="e902a-102">GetGeneratorSystemFunction function</span></span>

<span data-ttu-id="e902a-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="e902a-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="e902a-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e902a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e902a-105">Ruft die- `GeneratorIndex` Funktion in einem ab `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="e902a-105">Retrieves the `GeneratorIndex` function in a `GeneratorSystem`.</span></span>

```qsharp
function GetGeneratorSystemFunction (generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem) : (Int -> Microsoft.Quantum.Simulation.GeneratorIndex)
```


## <a name="input"></a><span data-ttu-id="e902a-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e902a-106">Input</span></span>

### <a name="generatorsystem--generatorsystem"></a><span data-ttu-id="e902a-107">Generatorsystem: [Generatorsystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="e902a-107">generatorSystem : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="e902a-108">Die gewünschte `GeneratorSystem`.</span><span class="sxs-lookup"><span data-stu-id="e902a-108">The `GeneratorSystem` of interest.</span></span>



## <a name="output--int---generatorindex"></a><span data-ttu-id="e902a-109">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int) -> [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="e902a-109">Output : [Int](xref:microsoft.quantum.lang-ref.int) -> [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="e902a-110">Eine Funktion, die jeden `GeneratorIndex` Begriff in einer hamiltonan indiziert.</span><span class="sxs-lookup"><span data-stu-id="e902a-110">An function that indexes each `GeneratorIndex` term in a Hamiltonian.</span></span>

## <a name="see-also"></a><span data-ttu-id="e902a-111">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e902a-111">See Also</span></span>

- [<span data-ttu-id="e902a-112">Microsoft. Quantum. Simulation. generatorindex</span><span class="sxs-lookup"><span data-stu-id="e902a-112">Microsoft.Quantum.Simulation.GeneratorIndex</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorIndex)
- [<span data-ttu-id="e902a-113">Microsoft. Quantum. Simulation. Generatorsystem</span><span class="sxs-lookup"><span data-stu-id="e902a-113">Microsoft.Quantum.Simulation.GeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorSystem)
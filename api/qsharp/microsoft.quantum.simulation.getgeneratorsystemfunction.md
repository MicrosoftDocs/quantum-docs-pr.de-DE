---
uid: Microsoft.Quantum.Simulation.GetGeneratorSystemFunction
title: Getgeneratorsystemfunction-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: GetGeneratorSystemFunction
qsharp.summary: Retrieves the `GeneratorIndex` function in a `GeneratorSystem`.
ms.openlocfilehash: 28e3c12d0ae0b08fc368c25eeb6f38d2834ca912
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229306"
---
# <a name="getgeneratorsystemfunction-function"></a><span data-ttu-id="995fc-102">Getgeneratorsystemfunction-Funktion</span><span class="sxs-lookup"><span data-stu-id="995fc-102">GetGeneratorSystemFunction function</span></span>

<span data-ttu-id="995fc-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="995fc-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="995fc-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="995fc-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="995fc-105">Ruft die- `GeneratorIndex` Funktion in einem ab `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="995fc-105">Retrieves the `GeneratorIndex` function in a `GeneratorSystem`.</span></span>

```qsharp
function GetGeneratorSystemFunction (generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem) : (Int -> Microsoft.Quantum.Simulation.GeneratorIndex)
```


## <a name="input"></a><span data-ttu-id="995fc-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="995fc-106">Input</span></span>

### <a name="generatorsystem--generatorsystem"></a><span data-ttu-id="995fc-107">Generatorsystem: [Generatorsystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="995fc-107">generatorSystem : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="995fc-108">Die gewünschte `GeneratorSystem`.</span><span class="sxs-lookup"><span data-stu-id="995fc-108">The `GeneratorSystem` of interest.</span></span>



## <a name="output--int---generatorindex"></a><span data-ttu-id="995fc-109">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int) -> [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="995fc-109">Output : [Int](xref:microsoft.quantum.lang-ref.int) -> [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="995fc-110">Eine Funktion, die jeden `GeneratorIndex` Begriff in einer hamiltonan indiziert.</span><span class="sxs-lookup"><span data-stu-id="995fc-110">An function that indexes each `GeneratorIndex` term in a Hamiltonian.</span></span>

## <a name="see-also"></a><span data-ttu-id="995fc-111">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="995fc-111">See Also</span></span>

- [<span data-ttu-id="995fc-112">Microsoft. Quantum. Simulation. generatorindex</span><span class="sxs-lookup"><span data-stu-id="995fc-112">Microsoft.Quantum.Simulation.GeneratorIndex</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorIndex)
- [<span data-ttu-id="995fc-113">Microsoft. Quantum. Simulation. Generatorsystem</span><span class="sxs-lookup"><span data-stu-id="995fc-113">Microsoft.Quantum.Simulation.GeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorSystem)
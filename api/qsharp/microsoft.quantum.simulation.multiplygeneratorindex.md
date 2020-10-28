---
uid: Microsoft.Quantum.Simulation.MultiplyGeneratorIndex
title: Multiplygeneratorindex-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: MultiplyGeneratorIndex
qsharp.summary: Multiplies the coefficient in a `GeneratorIndex`.
ms.openlocfilehash: 9ee0568073b65b027cc98eb56934e9286b59c27f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724488"
---
# <a name="multiplygeneratorindex-function"></a><span data-ttu-id="e4d3a-102">Multiplygeneratorindex-Funktion</span><span class="sxs-lookup"><span data-stu-id="e4d3a-102">MultiplyGeneratorIndex function</span></span>

<span data-ttu-id="e4d3a-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="e4d3a-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="e4d3a-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e4d3a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e4d3a-105">Multipliziert den Koeffizienten in einer `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="e4d3a-105">Multiplies the coefficient in a `GeneratorIndex`.</span></span>

```qsharp
function MultiplyGeneratorIndex (multiplier : Double, generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a><span data-ttu-id="e4d3a-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e4d3a-106">Input</span></span>

### <a name="multiplier--double"></a><span data-ttu-id="e4d3a-107">Multiplikator: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="e4d3a-107">multiplier : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="e4d3a-108">Der Multiplikator des Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="e4d3a-108">The multiplier on the coefficient.</span></span>


### <a name="generatorindex--generatorindex"></a><span data-ttu-id="e4d3a-109">generatorindex: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="e4d3a-109">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="e4d3a-110">Die zu multiplizierende `GeneratorIndex`.</span><span class="sxs-lookup"><span data-stu-id="e4d3a-110">The `GeneratorIndex` to be multiplied.</span></span>



## <a name="output--generatorindex"></a><span data-ttu-id="e4d3a-111">Ausgabe: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="e4d3a-111">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="e4d3a-112">Ein, der `GeneratorIndex` einen Begriff mit einem anderen Faktor darstellt `multiplier` .</span><span class="sxs-lookup"><span data-stu-id="e4d3a-112">A `GeneratorIndex` representing a term with coefficient a factor `multiplier` larger.</span></span>

## <a name="see-also"></a><span data-ttu-id="e4d3a-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e4d3a-113">See Also</span></span>

- [<span data-ttu-id="e4d3a-114">Microsoft. Quantum. Simulation. generatorindex</span><span class="sxs-lookup"><span data-stu-id="e4d3a-114">Microsoft.Quantum.Simulation.GeneratorIndex</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorIndex)
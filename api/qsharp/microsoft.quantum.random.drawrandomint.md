---
uid: Microsoft.Quantum.Random.DrawRandomInt
title: Drawrandomint-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomInt
qsharp.summary: Draws a random integer in a given inclusive range.
ms.openlocfilehash: d9d8d9fbb25587ac5ccbd4edf0e555649380375f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724656"
---
# <a name="drawrandomint-operation"></a><span data-ttu-id="d9264-102">Drawrandomint-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d9264-102">DrawRandomInt operation</span></span>

<span data-ttu-id="d9264-103">Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="d9264-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="d9264-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d9264-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d9264-105">Zeichnet eine zufällige ganze Zahl in einem angegebenen inklusiven Bereich.</span><span class="sxs-lookup"><span data-stu-id="d9264-105">Draws a random integer in a given inclusive range.</span></span>

```qsharp
operation DrawRandomInt (min : Int, max : Int) : Int
```


## <a name="input"></a><span data-ttu-id="d9264-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d9264-106">Input</span></span>

### <a name="min--int"></a><span data-ttu-id="d9264-107">Min: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d9264-107">min : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d9264-108">Die kleinste Ganzzahl, die gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9264-108">The smallest integer to be drawn.</span></span>


### <a name="max--int"></a><span data-ttu-id="d9264-109">Max: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d9264-109">max : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d9264-110">Die größte Ganzzahl, die gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9264-110">The largest integer to be drawn.</span></span>



## <a name="output--int"></a><span data-ttu-id="d9264-111">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d9264-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d9264-112">Eine ganze Zahl im inklusiven Bereich von `min` bis `max` mit einheitlicher Wahrscheinlichkeit.</span><span class="sxs-lookup"><span data-stu-id="d9264-112">An integer in the inclusive range from `min` to `max` with uniform probability.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9264-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d9264-113">Remarks</span></span>

<span data-ttu-id="d9264-114">Schlägt fehl, wenn `max <= min` .</span><span class="sxs-lookup"><span data-stu-id="d9264-114">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="d9264-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d9264-115">See Also</span></span>

- [<span data-ttu-id="d9264-116">Microsoft. Quantum. diskreteunifordistribution</span><span class="sxs-lookup"><span data-stu-id="d9264-116">Microsoft.Quantum.DiscreteUniformDistribution</span></span>](xref:Microsoft.Quantum.DiscreteUniformDistribution)
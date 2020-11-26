---
uid: Microsoft.Quantum.Random.DrawRandomInt
title: Drawrandomint-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomInt
qsharp.summary: Draws a random integer in a given inclusive range.
ms.openlocfilehash: f7b6cb75f761e4c45295245ed4bd4fb82c592809
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192909"
---
# <a name="drawrandomint-operation"></a><span data-ttu-id="30f07-102">Drawrandomint-Vorgang</span><span class="sxs-lookup"><span data-stu-id="30f07-102">DrawRandomInt operation</span></span>

<span data-ttu-id="30f07-103">Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="30f07-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="30f07-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="30f07-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="30f07-105">Zeichnet eine zufällige ganze Zahl in einem angegebenen inklusiven Bereich.</span><span class="sxs-lookup"><span data-stu-id="30f07-105">Draws a random integer in a given inclusive range.</span></span>

```qsharp
operation DrawRandomInt (min : Int, max : Int) : Int
```


## <a name="input"></a><span data-ttu-id="30f07-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="30f07-106">Input</span></span>

### <a name="min--int"></a><span data-ttu-id="30f07-107">Min: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="30f07-107">min : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="30f07-108">Die kleinste Ganzzahl, die gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="30f07-108">The smallest integer to be drawn.</span></span>


### <a name="max--int"></a><span data-ttu-id="30f07-109">Max: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="30f07-109">max : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="30f07-110">Die größte Ganzzahl, die gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="30f07-110">The largest integer to be drawn.</span></span>



## <a name="output--int"></a><span data-ttu-id="30f07-111">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="30f07-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="30f07-112">Eine ganze Zahl im inklusiven Bereich von `min` bis `max` mit einheitlicher Wahrscheinlichkeit.</span><span class="sxs-lookup"><span data-stu-id="30f07-112">An integer in the inclusive range from `min` to `max` with uniform probability.</span></span>

## <a name="remarks"></a><span data-ttu-id="30f07-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30f07-113">Remarks</span></span>

<span data-ttu-id="30f07-114">Schlägt fehl, wenn `max <= min` .</span><span class="sxs-lookup"><span data-stu-id="30f07-114">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="30f07-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="30f07-115">See Also</span></span>

- [<span data-ttu-id="30f07-116">Microsoft. Quantum. diskreteunifordistribution</span><span class="sxs-lookup"><span data-stu-id="30f07-116">Microsoft.Quantum.DiscreteUniformDistribution</span></span>](xref:Microsoft.Quantum.DiscreteUniformDistribution)
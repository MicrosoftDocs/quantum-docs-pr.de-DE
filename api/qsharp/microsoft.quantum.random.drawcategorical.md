---
uid: Microsoft.Quantum.Random.DrawCategorical
title: Drawcategorical-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawCategorical
qsharp.summary: Draws a random sample from a categorical distribution specified by a list of probablities.
ms.openlocfilehash: a5826aa5f658fea766db0ca5ccbb9c0d7d056d4c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192994"
---
# <a name="drawcategorical-operation"></a><span data-ttu-id="7af0b-102">Drawcategorical-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7af0b-102">DrawCategorical operation</span></span>

<span data-ttu-id="7af0b-103">Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="7af0b-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="7af0b-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="7af0b-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="7af0b-105">Zeichnet eine zufällige Stichprobe aus einer kategorischen Verteilung, die durch eine Liste von Wahrscheinlichkeiten angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7af0b-105">Draws a random sample from a categorical distribution specified by a list of probablities.</span></span>

```qsharp
operation DrawCategorical (probs : Double[]) : Int
```


## <a name="description"></a><span data-ttu-id="7af0b-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7af0b-106">Description</span></span>

<span data-ttu-id="7af0b-107">Die Wahrscheinlichkeit für die Auswahl eines bestimmten Indexes ist proportional zum Wert des Array Elements an diesem Index.</span><span class="sxs-lookup"><span data-stu-id="7af0b-107">The probability of selecting a specific index is proportional to the value of the array element at that index.</span></span>
<span data-ttu-id="7af0b-108">Array Elemente, die gleich 0 (null) sind, werden ignoriert, und ihre Indizes werden nie zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7af0b-108">Array elements that are equal to zero are ignored and their indices are never returned.</span></span> <span data-ttu-id="7af0b-109">Wenn ein Array Element kleiner als 0 (null) ist, oder wenn kein Array Element größer als 0 (null) ist, schlägt der Vorgang fehl.</span><span class="sxs-lookup"><span data-stu-id="7af0b-109">If any array element is less than zero, or if no array element is greater than zero, then the operation fails.</span></span>

## <a name="input"></a><span data-ttu-id="7af0b-110">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7af0b-110">Input</span></span>

### <a name="probs--double"></a><span data-ttu-id="7af0b-111">probs: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="7af0b-111">probs : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="7af0b-112">Ein Array von Gleit Komma Zahlen proportional zu der Wahrscheinlichkeit, dass die einzelnen Indizes ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="7af0b-112">An array of floating-point numbers proportional to the probability of selecting each index.</span></span>



## <a name="output--int"></a><span data-ttu-id="7af0b-113">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7af0b-113">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="7af0b-114">Eine ganze Zahl $i $ mit der Wahrscheinlichkeitswert $ \pr (i) = p_i/\ sum_i p_i $, wobei $p _I $ das $i $ th-Element von ist `probs` .</span><span class="sxs-lookup"><span data-stu-id="7af0b-114">An integer $i$ with probability $\Pr(i) = p_i / \sum_i p_i$, where $p_i$ is the $i$th element of `probs`.</span></span>

## <a name="see-also"></a><span data-ttu-id="7af0b-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7af0b-115">See Also</span></span>

- [<span data-ttu-id="7af0b-116">Microsoft. Quantum. Random. kategoricaldistribution</span><span class="sxs-lookup"><span data-stu-id="7af0b-116">Microsoft.Quantum.Random.CategoricalDistribution</span></span>](xref:Microsoft.Quantum.Random.CategoricalDistribution)
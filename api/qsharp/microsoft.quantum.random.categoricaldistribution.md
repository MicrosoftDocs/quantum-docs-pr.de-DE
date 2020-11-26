---
uid: Microsoft.Quantum.Random.CategoricalDistribution
title: Kategoricaldistribution-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: CategoricalDistribution
qsharp.summary: Returns a discrete categorical distribution, in which the probability for each of a finite list of given outcomes is explicitly specified.
ms.openlocfilehash: 2e3d9b17939d5a9a5bc5e7d89a843e0ff5a848ba
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210249"
---
# <a name="categoricaldistribution-function"></a><span data-ttu-id="d0d52-102">Kategoricaldistribution-Funktion</span><span class="sxs-lookup"><span data-stu-id="d0d52-102">CategoricalDistribution function</span></span>

<span data-ttu-id="d0d52-103">Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="d0d52-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="d0d52-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="d0d52-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="d0d52-105">Gibt eine diskrete kategorische Verteilung zurück, bei der die Wahrscheinlichkeit für jede endliche Liste der angegebenen Ergebnisse explizit angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d0d52-105">Returns a discrete categorical distribution, in which the probability for each of a finite list of given outcomes is explicitly specified.</span></span>

```qsharp
function CategoricalDistribution (probs : Double[]) : Microsoft.Quantum.Random.DiscreteDistribution
```


## <a name="input"></a><span data-ttu-id="d0d52-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d0d52-106">Input</span></span>

### <a name="probs--double"></a><span data-ttu-id="d0d52-107">probs: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="d0d52-107">probs : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="d0d52-108">Die Wahrscheinlichkeiten für die einzelnen Ergebnisse aus der kategorischen Verteilung.</span><span class="sxs-lookup"><span data-stu-id="d0d52-108">The probabilities for each outcome from the categorical distribution.</span></span>
<span data-ttu-id="d0d52-109">Diese Wahrscheinlichkeiten werden möglicherweise nicht normalisiert, müssen jedoch alle nicht negativ sein.</span><span class="sxs-lookup"><span data-stu-id="d0d52-109">These probabilities may not be normalized, but must all be non-negative.</span></span>



## <a name="output--discretedistribution"></a><span data-ttu-id="d0d52-110">Ausgabe: [diskretedistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span><span class="sxs-lookup"><span data-stu-id="d0d52-110">Output : [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span></span>

<span data-ttu-id="d0d52-111">Der Index `i` mit der Wahrscheinlichkeit `probs[i] / sum` , wobei `sum` die Summe von ist, die `probs` von angegeben wird `Fold(PlusD, 0.0, probs)` .</span><span class="sxs-lookup"><span data-stu-id="d0d52-111">The index `i` with probability `probs[i] / sum`, where `sum` is the sum of `probs` given by `Fold(PlusD, 0.0, probs)`.</span></span>
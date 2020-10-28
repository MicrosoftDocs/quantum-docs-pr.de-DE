---
uid: Microsoft.Quantum.Random.CategoricalDistribution
title: Kategoricaldistribution-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: CategoricalDistribution
qsharp.summary: Returns a discrete categorical distribution, in which the probability for each of a finite list of given outcomes is explicitly specified.
ms.openlocfilehash: 756e9e95cac5554ab8f885dab7c47ac1b174c0f3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722821"
---
# <a name="categoricaldistribution-function"></a><span data-ttu-id="f3470-102">Kategoricaldistribution-Funktion</span><span class="sxs-lookup"><span data-stu-id="f3470-102">CategoricalDistribution function</span></span>

<span data-ttu-id="f3470-103">Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="f3470-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="f3470-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f3470-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f3470-105">Gibt eine diskrete kategorische Verteilung zurück, bei der die Wahrscheinlichkeit für jede endliche Liste der angegebenen Ergebnisse explizit angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f3470-105">Returns a discrete categorical distribution, in which the probability for each of a finite list of given outcomes is explicitly specified.</span></span>

```qsharp
function CategoricalDistribution (probs : Double[]) : Microsoft.Quantum.Random.DiscreteDistribution
```


## <a name="input"></a><span data-ttu-id="f3470-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f3470-106">Input</span></span>

### <a name="probs--double"></a><span data-ttu-id="f3470-107">probs: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="f3470-107">probs : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="f3470-108">Die Wahrscheinlichkeiten für die einzelnen Ergebnisse aus der kategorischen Verteilung.</span><span class="sxs-lookup"><span data-stu-id="f3470-108">The probabilities for each outcome from the categorical distribution.</span></span>
<span data-ttu-id="f3470-109">Diese Wahrscheinlichkeiten werden möglicherweise nicht normalisiert, müssen jedoch alle nicht negativ sein.</span><span class="sxs-lookup"><span data-stu-id="f3470-109">These probabilities may not be normalized, but must all be non-negative.</span></span>



## <a name="output--discretedistribution"></a><span data-ttu-id="f3470-110">Ausgabe: [diskretedistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span><span class="sxs-lookup"><span data-stu-id="f3470-110">Output : [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span></span>

<span data-ttu-id="f3470-111">Der Index `i` mit der Wahrscheinlichkeit `probs[i] / sum` , wobei `sum` die Summe von ist, die `probs` von angegeben wird `Fold(PlusD, 0.0, probs)` .</span><span class="sxs-lookup"><span data-stu-id="f3470-111">The index `i` with probability `probs[i] / sum`, where `sum` is the sum of `probs` given by `Fold(PlusD, 0.0, probs)`.</span></span>
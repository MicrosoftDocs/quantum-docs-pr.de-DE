---
uid: Microsoft.Quantum.Random.CategoricalDistribution
title: Kategoricaldistribution-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: CategoricalDistribution
qsharp.summary: Returns a discrete categorical distribution, in which the probability for each of a finite list of given outcomes is explicitly specified.
ms.openlocfilehash: 754ada71078bd5446f78885ace31d92dce6bf1a4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842346"
---
# <a name="categoricaldistribution-function"></a><span data-ttu-id="ee276-102">Kategoricaldistribution-Funktion</span><span class="sxs-lookup"><span data-stu-id="ee276-102">CategoricalDistribution function</span></span>

<span data-ttu-id="ee276-103">Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="ee276-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="ee276-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="ee276-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="ee276-105">Gibt eine diskrete kategorische Verteilung zurück, bei der die Wahrscheinlichkeit für jede endliche Liste der angegebenen Ergebnisse explizit angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ee276-105">Returns a discrete categorical distribution, in which the probability for each of a finite list of given outcomes is explicitly specified.</span></span>

```qsharp
function CategoricalDistribution (probs : Double[]) : Microsoft.Quantum.Random.DiscreteDistribution
```


## <a name="input"></a><span data-ttu-id="ee276-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ee276-106">Input</span></span>

### <a name="probs--double"></a><span data-ttu-id="ee276-107">probs: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="ee276-107">probs : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="ee276-108">Die Wahrscheinlichkeiten für die einzelnen Ergebnisse aus der kategorischen Verteilung.</span><span class="sxs-lookup"><span data-stu-id="ee276-108">The probabilities for each outcome from the categorical distribution.</span></span>
<span data-ttu-id="ee276-109">Diese Wahrscheinlichkeiten werden möglicherweise nicht normalisiert, müssen jedoch alle nicht negativ sein.</span><span class="sxs-lookup"><span data-stu-id="ee276-109">These probabilities may not be normalized, but must all be non-negative.</span></span>



## <a name="output--discretedistribution"></a><span data-ttu-id="ee276-110">Ausgabe: [diskretedistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span><span class="sxs-lookup"><span data-stu-id="ee276-110">Output : [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span></span>

<span data-ttu-id="ee276-111">Der Index `i` mit der Wahrscheinlichkeit `probs[i] / sum` , wobei `sum` die Summe von ist, die `probs` von angegeben wird `Fold(PlusD, 0.0, probs)` .</span><span class="sxs-lookup"><span data-stu-id="ee276-111">The index `i` with probability `probs[i] / sum`, where `sum` is the sum of `probs` given by `Fold(PlusD, 0.0, probs)`.</span></span>

## <a name="example"></a><span data-ttu-id="ee276-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ee276-112">Example</span></span>

<span data-ttu-id="ee276-113">Im folgenden Q #-Code wird 0 mit der Wahrscheinlichkeit 30% und 1 mit der Wahrscheinlichkeit 70% angezeigt:</span><span class="sxs-lookup"><span data-stu-id="ee276-113">The following Q# code will display 0 with probability 30% and 1 with probability 70%:</span></span>

```qsharp
let dist = CategoricalDistribution([0.3, 0.7]);
Message($"Got sample: {dist::Sample()}");
```
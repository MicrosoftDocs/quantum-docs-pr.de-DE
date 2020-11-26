---
uid: Microsoft.Quantum.Random.DiscreteUniformDistribution
title: Diskreteunifordistribution-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DiscreteUniformDistribution
qsharp.summary: Returns a uniform distribution over a given inclusive range.
ms.openlocfilehash: 08a62805f59df339ef6b91dff802c40c407808f4
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193011"
---
# <a name="discreteuniformdistribution-function"></a><span data-ttu-id="ddb2d-102">Diskreteunifordistribution-Funktion</span><span class="sxs-lookup"><span data-stu-id="ddb2d-102">DiscreteUniformDistribution function</span></span>

<span data-ttu-id="ddb2d-103">Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="ddb2d-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="ddb2d-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="ddb2d-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="ddb2d-105">Gibt eine einheitliche Verteilung für einen angegebenen inklusiven Bereich zurück.</span><span class="sxs-lookup"><span data-stu-id="ddb2d-105">Returns a uniform distribution over a given inclusive range.</span></span>

```qsharp
function DiscreteUniformDistribution (min : Int, max : Int) : Microsoft.Quantum.Random.DiscreteDistribution
```


## <a name="input"></a><span data-ttu-id="ddb2d-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ddb2d-106">Input</span></span>

### <a name="min--int"></a><span data-ttu-id="ddb2d-107">Min: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ddb2d-107">min : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ddb2d-108">Die kleinste Ganzzahl, die gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ddb2d-108">The smallest integer to be drawn.</span></span>


### <a name="max--int"></a><span data-ttu-id="ddb2d-109">Max: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ddb2d-109">max : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ddb2d-110">Die größte Ganzzahl, die gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ddb2d-110">The largest integer to be drawn.</span></span>



## <a name="output--discretedistribution"></a><span data-ttu-id="ddb2d-111">Ausgabe: [diskretedistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span><span class="sxs-lookup"><span data-stu-id="ddb2d-111">Output : [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span></span>

<span data-ttu-id="ddb2d-112">Eine Verteilung, deren zufällige variate ganze Zahlen im inklusiven Bereich von `min` bis `max` mit einheitlicher Wahrscheinlichkeit sind.</span><span class="sxs-lookup"><span data-stu-id="ddb2d-112">A distribution whose random variates are integers in the inclusive range from `min` to `max` with uniform probability.</span></span>

## <a name="remarks"></a><span data-ttu-id="ddb2d-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ddb2d-113">Remarks</span></span>

<span data-ttu-id="ddb2d-114">Schlägt fehl, wenn `max <= min` .</span><span class="sxs-lookup"><span data-stu-id="ddb2d-114">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="ddb2d-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ddb2d-115">See Also</span></span>

- [<span data-ttu-id="ddb2d-116">Microsoft. Quantum. drawrandomdouble</span><span class="sxs-lookup"><span data-stu-id="ddb2d-116">Microsoft.Quantum.DrawRandomDouble</span></span>](xref:Microsoft.Quantum.DrawRandomDouble)
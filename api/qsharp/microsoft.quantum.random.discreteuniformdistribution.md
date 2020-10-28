---
uid: Microsoft.Quantum.Random.DiscreteUniformDistribution
title: Diskreteunifordistribution-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DiscreteUniformDistribution
qsharp.summary: Returns a uniform distribution over a given inclusive range.
ms.openlocfilehash: 5e93c66d891d9b6aec548c0cf266df35e6090c92
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706727"
---
# <a name="discreteuniformdistribution-function"></a><span data-ttu-id="9937d-102">Diskreteunifordistribution-Funktion</span><span class="sxs-lookup"><span data-stu-id="9937d-102">DiscreteUniformDistribution function</span></span>

<span data-ttu-id="9937d-103">Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="9937d-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="9937d-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9937d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9937d-105">Gibt eine einheitliche Verteilung für einen angegebenen inklusiven Bereich zurück.</span><span class="sxs-lookup"><span data-stu-id="9937d-105">Returns a uniform distribution over a given inclusive range.</span></span>

```qsharp
function DiscreteUniformDistribution (min : Int, max : Int) : Microsoft.Quantum.Random.DiscreteDistribution
```


## <a name="input"></a><span data-ttu-id="9937d-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9937d-106">Input</span></span>

### <a name="min--int"></a><span data-ttu-id="9937d-107">Min: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9937d-107">min : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9937d-108">Die kleinste Ganzzahl, die gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9937d-108">The smallest integer to be drawn.</span></span>


### <a name="max--int"></a><span data-ttu-id="9937d-109">Max: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9937d-109">max : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9937d-110">Die größte Ganzzahl, die gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9937d-110">The largest integer to be drawn.</span></span>



## <a name="output--discretedistribution"></a><span data-ttu-id="9937d-111">Ausgabe: [diskretedistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span><span class="sxs-lookup"><span data-stu-id="9937d-111">Output : [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span></span>

<span data-ttu-id="9937d-112">Eine Verteilung, deren zufällige variate ganze Zahlen im inklusiven Bereich von `min` bis `max` mit einheitlicher Wahrscheinlichkeit sind.</span><span class="sxs-lookup"><span data-stu-id="9937d-112">A distribution whose random variates are integers in the inclusive range from `min` to `max` with uniform probability.</span></span>

## <a name="remarks"></a><span data-ttu-id="9937d-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9937d-113">Remarks</span></span>

<span data-ttu-id="9937d-114">Schlägt fehl, wenn `max <= min` .</span><span class="sxs-lookup"><span data-stu-id="9937d-114">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="9937d-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9937d-115">See Also</span></span>

- [<span data-ttu-id="9937d-116">Microsoft. Quantum. drawrandomdouble</span><span class="sxs-lookup"><span data-stu-id="9937d-116">Microsoft.Quantum.DrawRandomDouble</span></span>](xref:Microsoft.Quantum.DrawRandomDouble)
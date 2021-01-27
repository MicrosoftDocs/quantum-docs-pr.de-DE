---
uid: Microsoft.Quantum.Random.DiscreteUniformDistribution
title: Diskreteunifordistribution-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DiscreteUniformDistribution
qsharp.summary: Returns a uniform distribution over a given inclusive range.
ms.openlocfilehash: f909e7def5439ec0feef4ca4dc0cf8ed12374dfe
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853719"
---
# <a name="discreteuniformdistribution-function"></a><span data-ttu-id="a05b6-102">Diskreteunifordistribution-Funktion</span><span class="sxs-lookup"><span data-stu-id="a05b6-102">DiscreteUniformDistribution function</span></span>

<span data-ttu-id="a05b6-103">Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="a05b6-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="a05b6-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="a05b6-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="a05b6-105">Gibt eine einheitliche Verteilung für einen angegebenen inklusiven Bereich zurück.</span><span class="sxs-lookup"><span data-stu-id="a05b6-105">Returns a uniform distribution over a given inclusive range.</span></span>

```qsharp
function DiscreteUniformDistribution (min : Int, max : Int) : Microsoft.Quantum.Random.DiscreteDistribution
```


## <a name="input"></a><span data-ttu-id="a05b6-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a05b6-106">Input</span></span>

### <a name="min--int"></a><span data-ttu-id="a05b6-107">Min: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a05b6-107">min : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a05b6-108">Die kleinste Ganzzahl, die gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a05b6-108">The smallest integer to be drawn.</span></span>


### <a name="max--int"></a><span data-ttu-id="a05b6-109">Max: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a05b6-109">max : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a05b6-110">Die größte Ganzzahl, die gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a05b6-110">The largest integer to be drawn.</span></span>



## <a name="output--discretedistribution"></a><span data-ttu-id="a05b6-111">Ausgabe: [diskretedistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span><span class="sxs-lookup"><span data-stu-id="a05b6-111">Output : [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span></span>

<span data-ttu-id="a05b6-112">Eine Verteilung, deren zufällige variate ganze Zahlen im inklusiven Bereich von `min` bis `max` mit einheitlicher Wahrscheinlichkeit sind.</span><span class="sxs-lookup"><span data-stu-id="a05b6-112">A distribution whose random variates are integers in the inclusive range from `min` to `max` with uniform probability.</span></span>

## <a name="example"></a><span data-ttu-id="a05b6-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a05b6-113">Example</span></span>

<span data-ttu-id="a05b6-114">Der folgende f #-Code Ausschnitt führt nach dem Zufallsprinzip zu einem sechsseitigen Würfel:</span><span class="sxs-lookup"><span data-stu-id="a05b6-114">The following Q# snippet randomly rolls a six-sided die:</span></span>

```qsharp
let dieDistribution = DiscreteUniformDistribution(1, 6);
let dieRoll = dieDistribution::Sample();
```

## <a name="remarks"></a><span data-ttu-id="a05b6-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a05b6-115">Remarks</span></span>

<span data-ttu-id="a05b6-116">Schlägt fehl, wenn `max <= min` .</span><span class="sxs-lookup"><span data-stu-id="a05b6-116">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="a05b6-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a05b6-117">See Also</span></span>

- [<span data-ttu-id="a05b6-118">Microsoft. Quantum. drawrandomdouble</span><span class="sxs-lookup"><span data-stu-id="a05b6-118">Microsoft.Quantum.DrawRandomDouble</span></span>](xref:Microsoft.Quantum.DrawRandomDouble)
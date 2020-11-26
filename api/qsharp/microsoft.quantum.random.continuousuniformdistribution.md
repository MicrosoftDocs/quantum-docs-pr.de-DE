---
uid: Microsoft.Quantum.Random.ContinuousUniformDistribution
title: Continuousunifordistribution-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: ContinuousUniformDistribution
qsharp.summary: Returns a uniform distribution over a given inclusive interval.
ms.openlocfilehash: a3911fe9962ce18daa239de0272c53d83344134a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193079"
---
# <a name="continuousuniformdistribution-function"></a><span data-ttu-id="00751-102">Continuousunifordistribution-Funktion</span><span class="sxs-lookup"><span data-stu-id="00751-102">ContinuousUniformDistribution function</span></span>

<span data-ttu-id="00751-103">Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="00751-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="00751-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="00751-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="00751-105">Gibt eine einheitliche Verteilung über ein bestimmtes inklusives Intervall zurück.</span><span class="sxs-lookup"><span data-stu-id="00751-105">Returns a uniform distribution over a given inclusive interval.</span></span>

```qsharp
function ContinuousUniformDistribution (min : Double, max : Double) : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="input"></a><span data-ttu-id="00751-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="00751-106">Input</span></span>

### <a name="min--double"></a><span data-ttu-id="00751-107">Min: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="00751-107">min : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="00751-108">Die kleinste reelle Zahl, die gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="00751-108">The smallest real number to be drawn.</span></span>


### <a name="max--double"></a><span data-ttu-id="00751-109">Max.: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="00751-109">max : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="00751-110">Die größte reelle Zahl, die gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="00751-110">The largest real number to be drawn.</span></span>



## <a name="output--continuousdistribution"></a><span data-ttu-id="00751-111">Ausgabe: [continuousdistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="00751-111">Output : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>

<span data-ttu-id="00751-112">Eine Verteilung, deren zufällige variate echte Zahlen im inklusiven Intervall von `min` bis `max` mit einheitlicher Wahrscheinlichkeit sind.</span><span class="sxs-lookup"><span data-stu-id="00751-112">A distribution whose random variates are real numbers in the inclusive interval from `min` to `max` with uniform probability.</span></span>

## <a name="remarks"></a><span data-ttu-id="00751-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="00751-113">Remarks</span></span>

<span data-ttu-id="00751-114">Schlägt fehl, wenn `max <= min` .</span><span class="sxs-lookup"><span data-stu-id="00751-114">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="00751-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="00751-115">See Also</span></span>

- [<span data-ttu-id="00751-116">Microsoft. Quantum. drawrandomdouble</span><span class="sxs-lookup"><span data-stu-id="00751-116">Microsoft.Quantum.DrawRandomDouble</span></span>](xref:Microsoft.Quantum.DrawRandomDouble)
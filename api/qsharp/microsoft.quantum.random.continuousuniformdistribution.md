---
uid: Microsoft.Quantum.Random.ContinuousUniformDistribution
title: Continuousunifordistribution-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: ContinuousUniformDistribution
qsharp.summary: Returns a uniform distribution over a given inclusive interval.
ms.openlocfilehash: c81eb433f50277c677756ee70d916f4856260c6d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842314"
---
# <a name="continuousuniformdistribution-function"></a><span data-ttu-id="86daf-102">Continuousunifordistribution-Funktion</span><span class="sxs-lookup"><span data-stu-id="86daf-102">ContinuousUniformDistribution function</span></span>

<span data-ttu-id="86daf-103">Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="86daf-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="86daf-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="86daf-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="86daf-105">Gibt eine einheitliche Verteilung über ein bestimmtes inklusives Intervall zurück.</span><span class="sxs-lookup"><span data-stu-id="86daf-105">Returns a uniform distribution over a given inclusive interval.</span></span>

```qsharp
function ContinuousUniformDistribution (min : Double, max : Double) : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="input"></a><span data-ttu-id="86daf-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="86daf-106">Input</span></span>

### <a name="min--double"></a><span data-ttu-id="86daf-107">Min: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="86daf-107">min : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="86daf-108">Die kleinste reelle Zahl, die gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="86daf-108">The smallest real number to be drawn.</span></span>


### <a name="max--double"></a><span data-ttu-id="86daf-109">Max.: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="86daf-109">max : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="86daf-110">Die größte reelle Zahl, die gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="86daf-110">The largest real number to be drawn.</span></span>



## <a name="output--continuousdistribution"></a><span data-ttu-id="86daf-111">Ausgabe: [continuousdistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="86daf-111">Output : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>

<span data-ttu-id="86daf-112">Eine Verteilung, deren zufällige variate echte Zahlen im inklusiven Intervall von `min` bis `max` mit einheitlicher Wahrscheinlichkeit sind.</span><span class="sxs-lookup"><span data-stu-id="86daf-112">A distribution whose random variates are real numbers in the inclusive interval from `min` to `max` with uniform probability.</span></span>

## <a name="example"></a><span data-ttu-id="86daf-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="86daf-113">Example</span></span>

<span data-ttu-id="86daf-114">Der folgende f #-Code Ausschnitt zeichnet nach dem Zufallsprinzip einen Winkel zwischen $0 $ und $2 \pi $:</span><span class="sxs-lookup"><span data-stu-id="86daf-114">The following Q# snippet randomly draws an angle between $0$ and $2 \pi$:</span></span>

```qsharp
let angleDistribution = ContinuousUniformDistribution(0.0, 2.0 * PI());
let angle = angleDistribution::Sample();
```

## <a name="remarks"></a><span data-ttu-id="86daf-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="86daf-115">Remarks</span></span>

<span data-ttu-id="86daf-116">Schlägt fehl, wenn `max <= min` .</span><span class="sxs-lookup"><span data-stu-id="86daf-116">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="86daf-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="86daf-117">See Also</span></span>

- [<span data-ttu-id="86daf-118">Microsoft. Quantum. drawrandomdouble</span><span class="sxs-lookup"><span data-stu-id="86daf-118">Microsoft.Quantum.DrawRandomDouble</span></span>](xref:Microsoft.Quantum.DrawRandomDouble)
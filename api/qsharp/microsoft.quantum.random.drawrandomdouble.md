---
uid: Microsoft.Quantum.Random.DrawRandomDouble
title: Drawrandomdouble-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomDouble
qsharp.summary: Draws a random real number in a given inclusive interval.
ms.openlocfilehash: 792e9c714b761b48618aec2091e167a359c2b522
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847624"
---
# <a name="drawrandomdouble-operation"></a><span data-ttu-id="377fe-102">Drawrandomdouble-Vorgang</span><span class="sxs-lookup"><span data-stu-id="377fe-102">DrawRandomDouble operation</span></span>

<span data-ttu-id="377fe-103">Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="377fe-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="377fe-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="377fe-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="377fe-105">Zeichnet eine zufällige reelle Zahl in einem angegebenen inklusiven Intervall.</span><span class="sxs-lookup"><span data-stu-id="377fe-105">Draws a random real number in a given inclusive interval.</span></span>

```qsharp
operation DrawRandomDouble (min : Double, max : Double) : Double
```


## <a name="input"></a><span data-ttu-id="377fe-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="377fe-106">Input</span></span>

### <a name="min--double"></a><span data-ttu-id="377fe-107">Min: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="377fe-107">min : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="377fe-108">Die kleinste reelle Zahl, die gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="377fe-108">The smallest real number to be drawn.</span></span>


### <a name="max--double"></a><span data-ttu-id="377fe-109">Max.: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="377fe-109">max : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="377fe-110">Die größte reelle Zahl, die gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="377fe-110">The largest real number to be drawn.</span></span>



## <a name="output--double"></a><span data-ttu-id="377fe-111">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="377fe-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="377fe-112">Eine zufällige reelle Zahl im inklusiven Intervall von `min` bis `max` mit einheitlicher Wahrscheinlichkeit.</span><span class="sxs-lookup"><span data-stu-id="377fe-112">A random real number in the inclusive interval from `min` to `max` with uniform probability.</span></span>

## <a name="example"></a><span data-ttu-id="377fe-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="377fe-113">Example</span></span>

<span data-ttu-id="377fe-114">Der folgende f #-Code Ausschnitt zeichnet nach dem Zufallsprinzip einen Winkel zwischen $0 $ und $2 \pi $:</span><span class="sxs-lookup"><span data-stu-id="377fe-114">The following Q# snippet randomly draws an angle between $0$ and $2 \pi$:</span></span>

```qsharp
let angle = DrawRandomDouble(0.0, 2.0 * PI());
```

## <a name="remarks"></a><span data-ttu-id="377fe-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="377fe-115">Remarks</span></span>

<span data-ttu-id="377fe-116">Schlägt fehl, wenn `max <= min` .</span><span class="sxs-lookup"><span data-stu-id="377fe-116">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="377fe-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="377fe-117">See Also</span></span>

- [<span data-ttu-id="377fe-118">Microsoft. Quantum. continuousunifordistribution</span><span class="sxs-lookup"><span data-stu-id="377fe-118">Microsoft.Quantum.ContinuousUniformDistribution</span></span>](xref:Microsoft.Quantum.ContinuousUniformDistribution)
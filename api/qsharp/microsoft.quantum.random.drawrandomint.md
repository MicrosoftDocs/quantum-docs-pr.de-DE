---
uid: Microsoft.Quantum.Random.DrawRandomInt
title: Drawrandomint-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomInt
qsharp.summary: Draws a random integer in a given inclusive range.
ms.openlocfilehash: ebed7f52b7c4a8c538ed9d718c486b5aa94a0327
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851135"
---
# <a name="drawrandomint-operation"></a><span data-ttu-id="d0bcd-102">Drawrandomint-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d0bcd-102">DrawRandomInt operation</span></span>

<span data-ttu-id="d0bcd-103">Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="d0bcd-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="d0bcd-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="d0bcd-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="d0bcd-105">Zeichnet eine zufällige ganze Zahl in einem angegebenen inklusiven Bereich.</span><span class="sxs-lookup"><span data-stu-id="d0bcd-105">Draws a random integer in a given inclusive range.</span></span>

```qsharp
operation DrawRandomInt (min : Int, max : Int) : Int
```


## <a name="input"></a><span data-ttu-id="d0bcd-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d0bcd-106">Input</span></span>

### <a name="min--int"></a><span data-ttu-id="d0bcd-107">Min: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d0bcd-107">min : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d0bcd-108">Die kleinste Ganzzahl, die gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d0bcd-108">The smallest integer to be drawn.</span></span>


### <a name="max--int"></a><span data-ttu-id="d0bcd-109">Max: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d0bcd-109">max : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d0bcd-110">Die größte Ganzzahl, die gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d0bcd-110">The largest integer to be drawn.</span></span>



## <a name="output--int"></a><span data-ttu-id="d0bcd-111">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d0bcd-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d0bcd-112">Eine ganze Zahl im inklusiven Bereich von `min` bis `max` mit einheitlicher Wahrscheinlichkeit.</span><span class="sxs-lookup"><span data-stu-id="d0bcd-112">An integer in the inclusive range from `min` to `max` with uniform probability.</span></span>

## <a name="example"></a><span data-ttu-id="d0bcd-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d0bcd-113">Example</span></span>

<span data-ttu-id="d0bcd-114">Der folgende f #-Code Ausschnitt führt nach dem Zufallsprinzip zu einem sechsseitigen Würfel:</span><span class="sxs-lookup"><span data-stu-id="d0bcd-114">The following Q# snippet randomly rolls a six-sided die:</span></span>

```qsharp
let roll = DrawRandomInt(1, 6);
```

## <a name="remarks"></a><span data-ttu-id="d0bcd-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d0bcd-115">Remarks</span></span>

<span data-ttu-id="d0bcd-116">Schlägt fehl, wenn `max <= min` .</span><span class="sxs-lookup"><span data-stu-id="d0bcd-116">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="d0bcd-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d0bcd-117">See Also</span></span>

- [<span data-ttu-id="d0bcd-118">Microsoft. Quantum. diskreteunifordistribution</span><span class="sxs-lookup"><span data-stu-id="d0bcd-118">Microsoft.Quantum.DiscreteUniformDistribution</span></span>](xref:Microsoft.Quantum.DiscreteUniformDistribution)
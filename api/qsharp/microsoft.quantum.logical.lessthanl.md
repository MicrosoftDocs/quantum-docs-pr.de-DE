---
uid: Microsoft.Quantum.Logical.LessThanL
title: Lessthanl-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanL
qsharp.summary: Returns true if and only if a number is less than another number.
ms.openlocfilehash: fde57bcd9960056461bddac54300c298def8f7d5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701460"
---
# <a name="lessthanl-function"></a><span data-ttu-id="3edde-102">Lessthanl-Funktion</span><span class="sxs-lookup"><span data-stu-id="3edde-102">LessThanL function</span></span>

<span data-ttu-id="3edde-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="3edde-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="3edde-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3edde-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3edde-105">Gibt nur dann true zurück, wenn eine Zahl kleiner als eine andere Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="3edde-105">Returns true if and only if a number is less than another number.</span></span>

```qsharp
function LessThanL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="3edde-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3edde-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="3edde-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="3edde-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="3edde-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="3edde-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="3edde-109">b: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="3edde-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="3edde-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="3edde-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="3edde-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="3edde-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="3edde-112">`true` , wenn und nur, wenn `a` streng kleiner als ist `b` .</span><span class="sxs-lookup"><span data-stu-id="3edde-112">`true` if and only if `a` is strictly less than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="3edde-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3edde-113">Remarks</span></span>

<span data-ttu-id="3edde-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="3edde-114">The following are equivalent:</span></span>

```Q#
let cond = a < b;
let cond = LessThanL(a, b);
```
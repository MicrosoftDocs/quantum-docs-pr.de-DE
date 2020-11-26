---
uid: Microsoft.Quantum.Logical.LessThanOrEqualI
title: Lessthanorequali-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanOrEqualI
qsharp.summary: Returns true if and only if a number is less than or equal to another number.
ms.openlocfilehash: b2974c9bc84d0b4366767f47682ab542f85063e2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197565"
---
# <a name="lessthanorequali-function"></a><span data-ttu-id="9ea20-102">Lessthanorequali-Funktion</span><span class="sxs-lookup"><span data-stu-id="9ea20-102">LessThanOrEqualI function</span></span>

<span data-ttu-id="9ea20-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="9ea20-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="9ea20-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9ea20-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9ea20-105">Gibt nur dann true zurück, wenn eine Zahl kleiner oder gleich einer anderen Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="9ea20-105">Returns true if and only if a number is less than or equal to another number.</span></span>

```qsharp
function LessThanOrEqualI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="9ea20-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9ea20-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="9ea20-107">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9ea20-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9ea20-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="9ea20-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="9ea20-109">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9ea20-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9ea20-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="9ea20-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="9ea20-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="9ea20-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="9ea20-112">`true``a`, wenn kleiner oder gleich ist `b` .</span><span class="sxs-lookup"><span data-stu-id="9ea20-112">`true` if and only if `a` is less than or equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ea20-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9ea20-113">Remarks</span></span>

<span data-ttu-id="9ea20-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="9ea20-114">The following are equivalent:</span></span>

```Q#
let cond = a <= b;
let cond = LessThanOrEqualI(a, b);
```
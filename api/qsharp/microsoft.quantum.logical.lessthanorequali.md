---
uid: Microsoft.Quantum.Logical.LessThanOrEqualI
title: Lessthanorequali-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanOrEqualI
qsharp.summary: Returns true if and only if a number is less than or equal to another number.
ms.openlocfilehash: dd934fde3fae9c1a43032b4b08ac03afa72798d1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701453"
---
# <a name="lessthanorequali-function"></a><span data-ttu-id="9458d-102">Lessthanorequali-Funktion</span><span class="sxs-lookup"><span data-stu-id="9458d-102">LessThanOrEqualI function</span></span>

<span data-ttu-id="9458d-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="9458d-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="9458d-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9458d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9458d-105">Gibt nur dann true zurück, wenn eine Zahl kleiner oder gleich einer anderen Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="9458d-105">Returns true if and only if a number is less than or equal to another number.</span></span>

```qsharp
function LessThanOrEqualI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="9458d-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9458d-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="9458d-107">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9458d-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9458d-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="9458d-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="9458d-109">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9458d-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9458d-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="9458d-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="9458d-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="9458d-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="9458d-112">`true``a`, wenn kleiner oder gleich ist `b` .</span><span class="sxs-lookup"><span data-stu-id="9458d-112">`true` if and only if `a` is less than or equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="9458d-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9458d-113">Remarks</span></span>

<span data-ttu-id="9458d-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="9458d-114">The following are equivalent:</span></span>

```Q#
let cond = a <= b;
let cond = LessThanOrEqualI(a, b);
```
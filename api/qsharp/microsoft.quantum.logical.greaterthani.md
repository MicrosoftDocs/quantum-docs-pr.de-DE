---
uid: Microsoft.Quantum.Logical.GreaterThanI
title: Greaterthani-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanI
qsharp.summary: Returns true if and only if a number is greater than another number.
ms.openlocfilehash: ffd00d8086654a2d783a351fe254fb2ee35b9184
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701472"
---
# <a name="greaterthani-function"></a><span data-ttu-id="6487b-102">Greaterthani-Funktion</span><span class="sxs-lookup"><span data-stu-id="6487b-102">GreaterThanI function</span></span>

<span data-ttu-id="6487b-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="6487b-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="6487b-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6487b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6487b-105">Gibt nur dann true zurück, wenn eine Zahl größer als eine andere Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="6487b-105">Returns true if and only if a number is greater than another number.</span></span>

```qsharp
function GreaterThanI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="6487b-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6487b-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="6487b-107">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6487b-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6487b-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="6487b-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="6487b-109">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6487b-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6487b-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="6487b-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="6487b-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="6487b-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="6487b-112">`true` , wenn und nur, wenn `a` streng größer als ist `b` .</span><span class="sxs-lookup"><span data-stu-id="6487b-112">`true` if and only if `a` is strictly greater than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="6487b-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6487b-113">Remarks</span></span>

<span data-ttu-id="6487b-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="6487b-114">The following are equivalent:</span></span>

```Q#
let cond = a > b;
let cond = GreaterThanI(a, b);
```
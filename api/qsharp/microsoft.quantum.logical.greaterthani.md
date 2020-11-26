---
uid: Microsoft.Quantum.Logical.GreaterThanI
title: Greaterthani-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanI
qsharp.summary: Returns true if and only if a number is greater than another number.
ms.openlocfilehash: 06cae04150f9f0164b06a4e3d4bb78242b41dc0b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197992"
---
# <a name="greaterthani-function"></a><span data-ttu-id="bce34-102">Greaterthani-Funktion</span><span class="sxs-lookup"><span data-stu-id="bce34-102">GreaterThanI function</span></span>

<span data-ttu-id="bce34-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="bce34-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="bce34-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="bce34-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="bce34-105">Gibt nur dann true zurück, wenn eine Zahl größer als eine andere Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="bce34-105">Returns true if and only if a number is greater than another number.</span></span>

```qsharp
function GreaterThanI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="bce34-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bce34-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="bce34-107">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="bce34-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="bce34-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="bce34-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="bce34-109">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="bce34-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="bce34-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="bce34-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="bce34-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="bce34-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="bce34-112">`true` , wenn und nur, wenn `a` streng größer als ist `b` .</span><span class="sxs-lookup"><span data-stu-id="bce34-112">`true` if and only if `a` is strictly greater than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="bce34-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bce34-113">Remarks</span></span>

<span data-ttu-id="bce34-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="bce34-114">The following are equivalent:</span></span>

```Q#
let cond = a > b;
let cond = GreaterThanI(a, b);
```
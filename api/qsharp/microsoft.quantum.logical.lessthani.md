---
uid: Microsoft.Quantum.Logical.LessThanI
title: Lessthani-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanI
qsharp.summary: Returns true if and only if a number is less than another number.
ms.openlocfilehash: 5d5b17c8481ccf58b8e4fc4bb958e0adbf6d8f00
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197771"
---
# <a name="lessthani-function"></a><span data-ttu-id="31c87-102">Lessthani-Funktion</span><span class="sxs-lookup"><span data-stu-id="31c87-102">LessThanI function</span></span>

<span data-ttu-id="31c87-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="31c87-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="31c87-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="31c87-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="31c87-105">Gibt nur dann true zurück, wenn eine Zahl kleiner als eine andere Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="31c87-105">Returns true if and only if a number is less than another number.</span></span>

```qsharp
function LessThanI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="31c87-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="31c87-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="31c87-107">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="31c87-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="31c87-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="31c87-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="31c87-109">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="31c87-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="31c87-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="31c87-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="31c87-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="31c87-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="31c87-112">`true` , wenn und nur, wenn `a` streng kleiner als ist `b` .</span><span class="sxs-lookup"><span data-stu-id="31c87-112">`true` if and only if `a` is strictly less than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="31c87-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="31c87-113">Remarks</span></span>

<span data-ttu-id="31c87-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="31c87-114">The following are equivalent:</span></span>

```Q#
let cond = a < b;
let cond = LessThanI(a, b);
```
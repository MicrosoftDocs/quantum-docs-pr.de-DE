---
uid: Microsoft.Quantum.Logical.GreaterThanOrEqualI
title: Greaterthanorequali-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanOrEqualI
qsharp.summary: Returns true if and only if a number is greater than or equal to another number.
ms.openlocfilehash: 0435aae4a824bd19d972e9f6b331260bbe21f692
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197788"
---
# <a name="greaterthanorequali-function"></a><span data-ttu-id="54006-102">Greaterthanorequali-Funktion</span><span class="sxs-lookup"><span data-stu-id="54006-102">GreaterThanOrEqualI function</span></span>

<span data-ttu-id="54006-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="54006-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="54006-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="54006-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="54006-105">Gibt nur dann true zurück, wenn eine Zahl größer als eine andere Zahl oder gleich einer anderen Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="54006-105">Returns true if and only if a number is greater than or equal to another number.</span></span>

```qsharp
function GreaterThanOrEqualI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="54006-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="54006-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="54006-107">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="54006-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="54006-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="54006-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="54006-109">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="54006-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="54006-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="54006-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="54006-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="54006-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="54006-112">`true``a`, wenn größer als oder gleich ist `b` .</span><span class="sxs-lookup"><span data-stu-id="54006-112">`true` if and only if `a` is greater than or is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="54006-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="54006-113">Remarks</span></span>

<span data-ttu-id="54006-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="54006-114">The following are equivalent:</span></span>

```Q#
let cond = a >= b;
let cond = GreaterThanOrEqualI(a, b);
```
---
uid: Microsoft.Quantum.Logical.LessThanOrEqualL
title: Lessthanorequall-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanOrEqualL
qsharp.summary: Returns true if and only if a number is less than or equal to another number.
ms.openlocfilehash: 2322ae4dd6025108d322d29770f42953213aa025
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197600"
---
# <a name="lessthanorequall-function"></a><span data-ttu-id="6b88d-102">Lessthanorequall-Funktion</span><span class="sxs-lookup"><span data-stu-id="6b88d-102">LessThanOrEqualL function</span></span>

<span data-ttu-id="6b88d-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="6b88d-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="6b88d-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6b88d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6b88d-105">Gibt nur dann true zurück, wenn eine Zahl kleiner oder gleich einer anderen Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="6b88d-105">Returns true if and only if a number is less than or equal to another number.</span></span>

```qsharp
function LessThanOrEqualL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="6b88d-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6b88d-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="6b88d-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="6b88d-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="6b88d-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="6b88d-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="6b88d-109">b: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="6b88d-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="6b88d-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="6b88d-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="6b88d-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="6b88d-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="6b88d-112">`true``a`, wenn kleiner oder gleich ist `b` .</span><span class="sxs-lookup"><span data-stu-id="6b88d-112">`true` if and only if `a` is less than or equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b88d-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b88d-113">Remarks</span></span>

<span data-ttu-id="6b88d-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="6b88d-114">The following are equivalent:</span></span>

```Q#
let cond = a <= b;
let cond = LessThanOrEqualL(a, b);
```
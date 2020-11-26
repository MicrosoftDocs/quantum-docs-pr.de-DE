---
uid: Microsoft.Quantum.Logical.EqualR
title: Equalr-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualR
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: d68b2f1a26bf318400d3c88b37d9aabcc38cbdfe
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198005"
---
# <a name="equalr-function"></a><span data-ttu-id="a24a7-102">Equalr-Funktion</span><span class="sxs-lookup"><span data-stu-id="a24a7-102">EqualR function</span></span>

<span data-ttu-id="a24a7-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="a24a7-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="a24a7-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a24a7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a24a7-105">Gibt nur dann true zurück, wenn zwei Eingaben gleich sind.</span><span class="sxs-lookup"><span data-stu-id="a24a7-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualR (a : Result, b : Result) : Bool
```


## <a name="input"></a><span data-ttu-id="a24a7-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a24a7-106">Input</span></span>

### <a name="a--__invalidresult__"></a><span data-ttu-id="a24a7-107">a: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="a24a7-107">a : __invalid<Result>__</span></span>

<span data-ttu-id="a24a7-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="a24a7-108">The first value to be compared.</span></span>


### <a name="b--__invalidresult__"></a><span data-ttu-id="a24a7-109">b: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="a24a7-109">b : __invalid<Result>__</span></span>

<span data-ttu-id="a24a7-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="a24a7-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="a24a7-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="a24a7-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="a24a7-112">`true``a`, wenn gleich ist `b` .</span><span class="sxs-lookup"><span data-stu-id="a24a7-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="a24a7-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a24a7-113">Remarks</span></span>

<span data-ttu-id="a24a7-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="a24a7-114">The following are equivalent:</span></span>

```Q#
let cond = a == b;
let cond = EqualR(a, b);
```
---
uid: Microsoft.Quantum.Logical.NotEqualR
title: Notequalr-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualR
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: 39601396a75d8c1b9193d4b8f34fa05466beff06
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848499"
---
# <a name="notequalr-function"></a><span data-ttu-id="92cf7-102">Notequalr-Funktion</span><span class="sxs-lookup"><span data-stu-id="92cf7-102">NotEqualR function</span></span>

<span data-ttu-id="92cf7-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="92cf7-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="92cf7-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="92cf7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="92cf7-105">Gibt nur dann true zurück, wenn zwei Eingaben nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="92cf7-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualR (a : Result, b : Result) : Bool
```


## <a name="input"></a><span data-ttu-id="92cf7-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="92cf7-106">Input</span></span>

### <a name="a--__invalidresult__"></a><span data-ttu-id="92cf7-107">a: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="92cf7-107">a : __invalid<Result>__</span></span>

<span data-ttu-id="92cf7-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="92cf7-108">The first value to be compared.</span></span>


### <a name="b--__invalidresult__"></a><span data-ttu-id="92cf7-109">b: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="92cf7-109">b : __invalid<Result>__</span></span>

<span data-ttu-id="92cf7-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="92cf7-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="92cf7-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="92cf7-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="92cf7-112">`true``a`, wenn nicht gleich ist `b` .</span><span class="sxs-lookup"><span data-stu-id="92cf7-112">`true` if and only if `a` is not equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="92cf7-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="92cf7-113">Remarks</span></span>

<span data-ttu-id="92cf7-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="92cf7-114">The following are equivalent:</span></span>

```qsharp
let cond = a != b;
let cond = NotEqualR(a, b);
```
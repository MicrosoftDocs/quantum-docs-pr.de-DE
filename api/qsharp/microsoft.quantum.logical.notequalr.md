---
uid: Microsoft.Quantum.Logical.NotEqualR
title: Notequalr-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualR
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: 06615c7ffb6aafc296077990dfca0ce25e1e00fa
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701393"
---
# <a name="notequalr-function"></a><span data-ttu-id="e0c5e-102">Notequalr-Funktion</span><span class="sxs-lookup"><span data-stu-id="e0c5e-102">NotEqualR function</span></span>

<span data-ttu-id="e0c5e-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="e0c5e-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="e0c5e-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e0c5e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e0c5e-105">Gibt nur dann true zurück, wenn zwei Eingaben nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="e0c5e-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualR (a : Result, b : Result) : Bool
```


## <a name="input"></a><span data-ttu-id="e0c5e-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e0c5e-106">Input</span></span>

### <a name="a--__invalidresult__"></a><span data-ttu-id="e0c5e-107">a: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="e0c5e-107">a : __invalid<Result>__</span></span>

<span data-ttu-id="e0c5e-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="e0c5e-108">The first value to be compared.</span></span>


### <a name="b--__invalidresult__"></a><span data-ttu-id="e0c5e-109">b: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="e0c5e-109">b : __invalid<Result>__</span></span>

<span data-ttu-id="e0c5e-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="e0c5e-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="e0c5e-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="e0c5e-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="e0c5e-112">`true``a`, wenn nicht gleich ist `b` .</span><span class="sxs-lookup"><span data-stu-id="e0c5e-112">`true` if and only if `a` is not equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0c5e-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e0c5e-113">Remarks</span></span>

<span data-ttu-id="e0c5e-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="e0c5e-114">The following are equivalent:</span></span>

```Q#
let cond = a != b;
let cond = NotEqualR(a, b);
```
---
uid: Microsoft.Quantum.Logical.EqualR
title: Equalr-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualR
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: 5aaa17303d75b27c3ac82cbe7d739a60016fdcb1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701495"
---
# <a name="equalr-function"></a><span data-ttu-id="38f46-102">Equalr-Funktion</span><span class="sxs-lookup"><span data-stu-id="38f46-102">EqualR function</span></span>

<span data-ttu-id="38f46-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="38f46-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="38f46-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="38f46-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="38f46-105">Gibt nur dann true zurück, wenn zwei Eingaben gleich sind.</span><span class="sxs-lookup"><span data-stu-id="38f46-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualR (a : Result, b : Result) : Bool
```


## <a name="input"></a><span data-ttu-id="38f46-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="38f46-106">Input</span></span>

### <a name="a--__invalidresult__"></a><span data-ttu-id="38f46-107">a: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="38f46-107">a : __invalid<Result>__</span></span>

<span data-ttu-id="38f46-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="38f46-108">The first value to be compared.</span></span>


### <a name="b--__invalidresult__"></a><span data-ttu-id="38f46-109">b: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="38f46-109">b : __invalid<Result>__</span></span>

<span data-ttu-id="38f46-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="38f46-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="38f46-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="38f46-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="38f46-112">`true``a`, wenn gleich ist `b` .</span><span class="sxs-lookup"><span data-stu-id="38f46-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="38f46-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="38f46-113">Remarks</span></span>

<span data-ttu-id="38f46-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="38f46-114">The following are equivalent:</span></span>

```Q#
let cond = a == b;
let cond = EqualR(a, b);
```
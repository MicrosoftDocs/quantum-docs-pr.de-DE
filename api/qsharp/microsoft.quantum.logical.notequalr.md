---
uid: Microsoft.Quantum.Logical.NotEqualR
title: Notequalr-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualR
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: 4ac6cf4b220fa42c8eb946d6fbcad4cdb191afcd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197193"
---
# <a name="notequalr-function"></a><span data-ttu-id="f1af5-102">Notequalr-Funktion</span><span class="sxs-lookup"><span data-stu-id="f1af5-102">NotEqualR function</span></span>

<span data-ttu-id="f1af5-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="f1af5-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="f1af5-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f1af5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f1af5-105">Gibt nur dann true zurück, wenn zwei Eingaben nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="f1af5-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualR (a : Result, b : Result) : Bool
```


## <a name="input"></a><span data-ttu-id="f1af5-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f1af5-106">Input</span></span>

### <a name="a--__invalidresult__"></a><span data-ttu-id="f1af5-107">a: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="f1af5-107">a : __invalid<Result>__</span></span>

<span data-ttu-id="f1af5-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="f1af5-108">The first value to be compared.</span></span>


### <a name="b--__invalidresult__"></a><span data-ttu-id="f1af5-109">b: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="f1af5-109">b : __invalid<Result>__</span></span>

<span data-ttu-id="f1af5-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="f1af5-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="f1af5-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="f1af5-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="f1af5-112">`true``a`, wenn nicht gleich ist `b` .</span><span class="sxs-lookup"><span data-stu-id="f1af5-112">`true` if and only if `a` is not equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1af5-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f1af5-113">Remarks</span></span>

<span data-ttu-id="f1af5-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="f1af5-114">The following are equivalent:</span></span>

```Q#
let cond = a != b;
let cond = NotEqualR(a, b);
```
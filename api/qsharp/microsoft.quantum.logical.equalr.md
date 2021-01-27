---
uid: Microsoft.Quantum.Logical.EqualR
title: Equalr-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualR
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: 9ce29f2868f092001a3dca23a2913a3963ac70fe
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98815965"
---
# <a name="equalr-function"></a><span data-ttu-id="64bf0-102">Equalr-Funktion</span><span class="sxs-lookup"><span data-stu-id="64bf0-102">EqualR function</span></span>

<span data-ttu-id="64bf0-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="64bf0-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="64bf0-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="64bf0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="64bf0-105">Gibt nur dann true zurück, wenn zwei Eingaben gleich sind.</span><span class="sxs-lookup"><span data-stu-id="64bf0-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualR (a : Result, b : Result) : Bool
```


## <a name="input"></a><span data-ttu-id="64bf0-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="64bf0-106">Input</span></span>

### <a name="a--__invalidresult__"></a><span data-ttu-id="64bf0-107">a: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="64bf0-107">a : __invalid<Result>__</span></span>

<span data-ttu-id="64bf0-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="64bf0-108">The first value to be compared.</span></span>


### <a name="b--__invalidresult__"></a><span data-ttu-id="64bf0-109">b: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="64bf0-109">b : __invalid<Result>__</span></span>

<span data-ttu-id="64bf0-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="64bf0-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="64bf0-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="64bf0-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="64bf0-112">`true``a`, wenn gleich ist `b` .</span><span class="sxs-lookup"><span data-stu-id="64bf0-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="64bf0-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64bf0-113">Remarks</span></span>

<span data-ttu-id="64bf0-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="64bf0-114">The following are equivalent:</span></span>

```qsharp
let cond = a == b;
let cond = EqualR(a, b);
```
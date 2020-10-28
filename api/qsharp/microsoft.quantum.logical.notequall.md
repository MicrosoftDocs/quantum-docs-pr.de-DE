---
uid: Microsoft.Quantum.Logical.NotEqualL
title: Notequall-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualL
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: f1d36c284293519e75e6c30ac64679c7bdf4609c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701399"
---
# <a name="notequall-function"></a><span data-ttu-id="0516f-102">Notequall-Funktion</span><span class="sxs-lookup"><span data-stu-id="0516f-102">NotEqualL function</span></span>

<span data-ttu-id="0516f-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="0516f-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="0516f-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0516f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0516f-105">Gibt nur dann true zurück, wenn zwei Eingaben nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="0516f-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="0516f-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0516f-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="0516f-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="0516f-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="0516f-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="0516f-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="0516f-109">b: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="0516f-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="0516f-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="0516f-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="0516f-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="0516f-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="0516f-112">`true``a`, wenn nicht gleich ist `b` .</span><span class="sxs-lookup"><span data-stu-id="0516f-112">`true` if and only if `a` is not equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="0516f-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0516f-113">Remarks</span></span>

<span data-ttu-id="0516f-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="0516f-114">The following are equivalent:</span></span>

```Q#
let cond = a != b;
let cond = NotEqualL(a, b);
```
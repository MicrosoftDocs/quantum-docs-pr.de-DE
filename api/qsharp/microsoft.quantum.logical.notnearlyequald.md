---
uid: Microsoft.Quantum.Logical.NotNearlyEqualD
title: Notnearlyequald-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotNearlyEqualD
qsharp.summary: Returns true if and only if two inputs are not nearly equal (that is, are not within a tolerance of 1e-12).
ms.openlocfilehash: 23229b1630982eba4485330cc2290aed733c4d86
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197142"
---
# <a name="notnearlyequald-function"></a><span data-ttu-id="a6d1f-102">Notnearlyequald-Funktion</span><span class="sxs-lookup"><span data-stu-id="a6d1f-102">NotNearlyEqualD function</span></span>

<span data-ttu-id="a6d1f-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="a6d1f-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="a6d1f-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a6d1f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a6d1f-105">Gibt nur dann true zurück, wenn zwei Eingaben nicht annähernd gleich sind (d. h. nicht innerhalb einer Toleranz von 1E-12).</span><span class="sxs-lookup"><span data-stu-id="a6d1f-105">Returns true if and only if two inputs are not nearly equal (that is, are not within a tolerance of 1e-12).</span></span>

```qsharp
function NotNearlyEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="a6d1f-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a6d1f-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="a6d1f-107">a: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="a6d1f-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="a6d1f-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="a6d1f-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="a6d1f-109">b: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="a6d1f-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="a6d1f-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="a6d1f-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="a6d1f-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="a6d1f-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="a6d1f-112">`true``a`, wenn nicht fast gleich ist `b` .</span><span class="sxs-lookup"><span data-stu-id="a6d1f-112">`true` if and only if `a` is not nearly equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6d1f-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a6d1f-113">Remarks</span></span>

<span data-ttu-id="a6d1f-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="a6d1f-114">The following are equivalent:</span></span>

```Q#
let cond = Microsoft.Quantum.Math.AbsD(a - b) >= 1e-12;
let cond = NotNearlyEqualD(a, b);
```
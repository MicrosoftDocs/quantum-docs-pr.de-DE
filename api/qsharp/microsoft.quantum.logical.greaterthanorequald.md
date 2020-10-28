---
uid: Microsoft.Quantum.Logical.GreaterThanOrEqualD
title: Greaterthanorequald-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanOrEqualD
qsharp.summary: Returns true if and only if a number is greater than or equal to another number.
ms.openlocfilehash: 9d794fa94c1ccbde4030c90198fd7c7654469876
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702071"
---
# <a name="greaterthanorequald-function"></a><span data-ttu-id="bfbf1-102">Greaterthanorequald-Funktion</span><span class="sxs-lookup"><span data-stu-id="bfbf1-102">GreaterThanOrEqualD function</span></span>

<span data-ttu-id="bfbf1-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="bfbf1-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="bfbf1-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="bfbf1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="bfbf1-105">Gibt nur dann true zurück, wenn eine Zahl größer als eine andere Zahl oder gleich einer anderen Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="bfbf1-105">Returns true if and only if a number is greater than or equal to another number.</span></span>

```qsharp
function GreaterThanOrEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="bfbf1-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bfbf1-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="bfbf1-107">a: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="bfbf1-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="bfbf1-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="bfbf1-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="bfbf1-109">b: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="bfbf1-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="bfbf1-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="bfbf1-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="bfbf1-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="bfbf1-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="bfbf1-112">`true``a`, wenn größer als oder gleich ist `b` .</span><span class="sxs-lookup"><span data-stu-id="bfbf1-112">`true` if and only if `a` is greater than or is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfbf1-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bfbf1-113">Remarks</span></span>

<span data-ttu-id="bfbf1-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="bfbf1-114">The following are equivalent:</span></span>

```Q#
let cond = a >= b;
let cond = GreaterThanOrEqualD(a, b);
```
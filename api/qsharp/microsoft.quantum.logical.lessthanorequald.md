---
uid: Microsoft.Quantum.Logical.LessThanOrEqualD
title: Lessthanorequald-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanOrEqualD
qsharp.summary: Returns true if and only if a number is less than or equal to another number.
ms.openlocfilehash: 7b0e9da379bd67eb78a80e7a535a15dcb8ba85c7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701459"
---
# <a name="lessthanorequald-function"></a><span data-ttu-id="f85a3-102">Lessthanorequald-Funktion</span><span class="sxs-lookup"><span data-stu-id="f85a3-102">LessThanOrEqualD function</span></span>

<span data-ttu-id="f85a3-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="f85a3-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="f85a3-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f85a3-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f85a3-105">Gibt nur dann true zurück, wenn eine Zahl kleiner oder gleich einer anderen Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="f85a3-105">Returns true if and only if a number is less than or equal to another number.</span></span>

```qsharp
function LessThanOrEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="f85a3-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f85a3-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="f85a3-107">a: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="f85a3-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="f85a3-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="f85a3-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="f85a3-109">b: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="f85a3-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="f85a3-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="f85a3-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="f85a3-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="f85a3-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="f85a3-112">`true``a`, wenn kleiner oder gleich ist `b` .</span><span class="sxs-lookup"><span data-stu-id="f85a3-112">`true` if and only if `a` is less than or equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="f85a3-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f85a3-113">Remarks</span></span>

<span data-ttu-id="f85a3-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="f85a3-114">The following are equivalent:</span></span>

```Q#
let cond = a <= b;
let cond = LessThanOrEqualD(a, b);
```
---
uid: Microsoft.Quantum.Logical.NearlyEqualD
title: Nearlyequald-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NearlyEqualD
qsharp.summary: Returns true if and only if two inputs are nearly equal (that is, within a tolerance of 1e-12).
ms.openlocfilehash: 332f9ea1753b539eba7b931d5b948b2a238d1abf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701424"
---
# <a name="nearlyequald-function"></a><span data-ttu-id="dc4d9-102">Nearlyequald-Funktion</span><span class="sxs-lookup"><span data-stu-id="dc4d9-102">NearlyEqualD function</span></span>

<span data-ttu-id="dc4d9-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="dc4d9-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="dc4d9-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="dc4d9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="dc4d9-105">Gibt nur dann true zurück, wenn zwei Eingaben fast gleich sind (d. h. innerhalb einer Toleranz von 1E-12).</span><span class="sxs-lookup"><span data-stu-id="dc4d9-105">Returns true if and only if two inputs are nearly equal (that is, within a tolerance of 1e-12).</span></span>

```qsharp
function NearlyEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="dc4d9-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dc4d9-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="dc4d9-107">a: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="dc4d9-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="dc4d9-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="dc4d9-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="dc4d9-109">b: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="dc4d9-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="dc4d9-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="dc4d9-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="dc4d9-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="dc4d9-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="dc4d9-112">`true` , wenn und nur `a` , wenn fast gleich ist `b` .</span><span class="sxs-lookup"><span data-stu-id="dc4d9-112">`true` if and only if `a` is nearly equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc4d9-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dc4d9-113">Remarks</span></span>

<span data-ttu-id="dc4d9-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="dc4d9-114">The following are equivalent:</span></span>

```Q#
let cond = Microsoft.Quantum.Math.AbsD(a - b) < 1e-12;
let cond = NearlyEqualD(a, b);
```
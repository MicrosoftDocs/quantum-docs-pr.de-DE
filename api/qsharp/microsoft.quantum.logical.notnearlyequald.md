---
uid: Microsoft.Quantum.Logical.NotNearlyEqualD
title: Notnearlyequald-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotNearlyEqualD
qsharp.summary: Returns true if and only if two inputs are not nearly equal (that is, are not within a tolerance of 1e-12).
ms.openlocfilehash: d9e4cc5b0cfba3989ae64e494d0daa52069718a4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707015"
---
# <a name="notnearlyequald-function"></a><span data-ttu-id="ee38b-102">Notnearlyequald-Funktion</span><span class="sxs-lookup"><span data-stu-id="ee38b-102">NotNearlyEqualD function</span></span>

<span data-ttu-id="ee38b-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="ee38b-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="ee38b-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ee38b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ee38b-105">Gibt nur dann true zurück, wenn zwei Eingaben nicht annähernd gleich sind (d. h. nicht innerhalb einer Toleranz von 1E-12).</span><span class="sxs-lookup"><span data-stu-id="ee38b-105">Returns true if and only if two inputs are not nearly equal (that is, are not within a tolerance of 1e-12).</span></span>

```qsharp
function NotNearlyEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="ee38b-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ee38b-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="ee38b-107">a: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="ee38b-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="ee38b-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="ee38b-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="ee38b-109">b: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="ee38b-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="ee38b-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="ee38b-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="ee38b-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="ee38b-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="ee38b-112">`true``a`, wenn nicht fast gleich ist `b` .</span><span class="sxs-lookup"><span data-stu-id="ee38b-112">`true` if and only if `a` is not nearly equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee38b-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ee38b-113">Remarks</span></span>

<span data-ttu-id="ee38b-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="ee38b-114">The following are equivalent:</span></span>

```Q#
let cond = Microsoft.Quantum.Math.AbsD(a - b) >= 1e-12;
let cond = NotNearlyEqualD(a, b);
```
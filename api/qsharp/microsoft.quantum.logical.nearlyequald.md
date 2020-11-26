---
uid: Microsoft.Quantum.Logical.NearlyEqualD
title: Nearlyequald-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NearlyEqualD
qsharp.summary: Returns true if and only if two inputs are nearly equal (that is, within a tolerance of 1e-12).
ms.openlocfilehash: 246fad15c691a53fcc5be10f2c713672e0b54e6b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197465"
---
# <a name="nearlyequald-function"></a><span data-ttu-id="66c14-102">Nearlyequald-Funktion</span><span class="sxs-lookup"><span data-stu-id="66c14-102">NearlyEqualD function</span></span>

<span data-ttu-id="66c14-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="66c14-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="66c14-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="66c14-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="66c14-105">Gibt nur dann true zurück, wenn zwei Eingaben fast gleich sind (d. h. innerhalb einer Toleranz von 1E-12).</span><span class="sxs-lookup"><span data-stu-id="66c14-105">Returns true if and only if two inputs are nearly equal (that is, within a tolerance of 1e-12).</span></span>

```qsharp
function NearlyEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="66c14-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="66c14-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="66c14-107">a: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="66c14-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="66c14-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="66c14-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="66c14-109">b: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="66c14-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="66c14-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="66c14-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="66c14-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="66c14-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="66c14-112">`true` , wenn und nur `a` , wenn fast gleich ist `b` .</span><span class="sxs-lookup"><span data-stu-id="66c14-112">`true` if and only if `a` is nearly equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="66c14-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="66c14-113">Remarks</span></span>

<span data-ttu-id="66c14-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="66c14-114">The following are equivalent:</span></span>

```Q#
let cond = Microsoft.Quantum.Math.AbsD(a - b) < 1e-12;
let cond = NearlyEqualD(a, b);
```
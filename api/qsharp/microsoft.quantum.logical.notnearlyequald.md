---
uid: Microsoft.Quantum.Logical.NotNearlyEqualD
title: Notnearlyequald-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotNearlyEqualD
qsharp.summary: Returns true if and only if two inputs are not nearly equal (that is, are not within a tolerance of 1e-12).
ms.openlocfilehash: 6e4cf3ec009f55ecc6345453c080520a3af6a8ef
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848483"
---
# <a name="notnearlyequald-function"></a><span data-ttu-id="702a5-102">Notnearlyequald-Funktion</span><span class="sxs-lookup"><span data-stu-id="702a5-102">NotNearlyEqualD function</span></span>

<span data-ttu-id="702a5-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="702a5-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="702a5-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="702a5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="702a5-105">Gibt nur dann true zurück, wenn zwei Eingaben nicht annähernd gleich sind (d. h. nicht innerhalb einer Toleranz von 1E-12).</span><span class="sxs-lookup"><span data-stu-id="702a5-105">Returns true if and only if two inputs are not nearly equal (that is, are not within a tolerance of 1e-12).</span></span>

```qsharp
function NotNearlyEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="702a5-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="702a5-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="702a5-107">a: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="702a5-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="702a5-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="702a5-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="702a5-109">b: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="702a5-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="702a5-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="702a5-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="702a5-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="702a5-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="702a5-112">`true``a`, wenn nicht fast gleich ist `b` .</span><span class="sxs-lookup"><span data-stu-id="702a5-112">`true` if and only if `a` is not nearly equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="702a5-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="702a5-113">Remarks</span></span>

<span data-ttu-id="702a5-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="702a5-114">The following are equivalent:</span></span>

```qsharp
let cond = Microsoft.Quantum.Math.AbsD(a - b) >= 1e-12;
let cond = NotNearlyEqualD(a, b);
```
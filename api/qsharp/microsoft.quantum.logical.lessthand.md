---
uid: Microsoft.Quantum.Logical.LessThanD
title: Lessthand-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanD
qsharp.summary: Returns true if and only if a number is less than another number.
ms.openlocfilehash: 8cd274d5e299df2f556006baf7457d54aebcd071
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723493"
---
# <a name="lessthand-function"></a><span data-ttu-id="bfb2b-102">Lessthand-Funktion</span><span class="sxs-lookup"><span data-stu-id="bfb2b-102">LessThanD function</span></span>

<span data-ttu-id="bfb2b-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="bfb2b-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="bfb2b-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="bfb2b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="bfb2b-105">Gibt nur dann true zurück, wenn eine Zahl kleiner als eine andere Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="bfb2b-105">Returns true if and only if a number is less than another number.</span></span>

```qsharp
function LessThanD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="bfb2b-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bfb2b-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="bfb2b-107">a: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="bfb2b-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="bfb2b-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="bfb2b-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="bfb2b-109">b: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="bfb2b-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="bfb2b-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="bfb2b-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="bfb2b-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="bfb2b-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="bfb2b-112">`true` , wenn und nur, wenn `a` streng kleiner als ist `b` .</span><span class="sxs-lookup"><span data-stu-id="bfb2b-112">`true` if and only if `a` is strictly less than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfb2b-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bfb2b-113">Remarks</span></span>

<span data-ttu-id="bfb2b-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="bfb2b-114">The following are equivalent:</span></span>

```Q#
let cond = a < b;
let cond = LessThanD(a, b);
```
---
uid: Microsoft.Quantum.Logical.LessThanD
title: Lessthand-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanD
qsharp.summary: Returns true if and only if a number is less than another number.
ms.openlocfilehash: 7135ed4b3414d143f5020496ae524bf89980a8a1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849170"
---
# <a name="lessthand-function"></a><span data-ttu-id="99ec3-102">Lessthand-Funktion</span><span class="sxs-lookup"><span data-stu-id="99ec3-102">LessThanD function</span></span>

<span data-ttu-id="99ec3-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="99ec3-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="99ec3-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="99ec3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="99ec3-105">Gibt nur dann true zurück, wenn eine Zahl kleiner als eine andere Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="99ec3-105">Returns true if and only if a number is less than another number.</span></span>

```qsharp
function LessThanD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="99ec3-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="99ec3-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="99ec3-107">a: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="99ec3-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="99ec3-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="99ec3-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="99ec3-109">b: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="99ec3-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="99ec3-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="99ec3-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="99ec3-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="99ec3-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="99ec3-112">`true` , wenn und nur, wenn `a` streng kleiner als ist `b` .</span><span class="sxs-lookup"><span data-stu-id="99ec3-112">`true` if and only if `a` is strictly less than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="99ec3-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="99ec3-113">Remarks</span></span>

<span data-ttu-id="99ec3-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="99ec3-114">The following are equivalent:</span></span>

```qsharp
let cond = a < b;
let cond = LessThanD(a, b);
```
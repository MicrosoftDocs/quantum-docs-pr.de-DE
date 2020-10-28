---
uid: Microsoft.Quantum.Logical.GreaterThanD
title: Greaterthand-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanD
qsharp.summary: Returns true if and only if a number is greater than another number.
ms.openlocfilehash: 20414e80e08993a18331a8f0b385a1e4cc1255b3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701483"
---
# <a name="greaterthand-function"></a><span data-ttu-id="11641-102">Greaterthand-Funktion</span><span class="sxs-lookup"><span data-stu-id="11641-102">GreaterThanD function</span></span>

<span data-ttu-id="11641-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="11641-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="11641-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="11641-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="11641-105">Gibt nur dann true zurück, wenn eine Zahl größer als eine andere Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="11641-105">Returns true if and only if a number is greater than another number.</span></span>

```qsharp
function GreaterThanD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="11641-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="11641-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="11641-107">a: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="11641-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="11641-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="11641-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="11641-109">b: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="11641-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="11641-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="11641-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="11641-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="11641-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="11641-112">`true` , wenn und nur, wenn `a` streng größer als ist `b` .</span><span class="sxs-lookup"><span data-stu-id="11641-112">`true` if and only if `a` is strictly greater than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="11641-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="11641-113">Remarks</span></span>

<span data-ttu-id="11641-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="11641-114">The following are equivalent:</span></span>

```Q#
let cond = a > b;
let cond = GreaterThanD(a, b);
```
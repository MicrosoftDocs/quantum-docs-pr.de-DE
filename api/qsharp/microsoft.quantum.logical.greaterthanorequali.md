---
uid: Microsoft.Quantum.Logical.GreaterThanOrEqualI
title: Greaterthanorequali-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanOrEqualI
qsharp.summary: Returns true if and only if a number is greater than or equal to another number.
ms.openlocfilehash: 292599c18d2aac44cef8f0eecca38eb1fbe22061
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723494"
---
# <a name="greaterthanorequali-function"></a><span data-ttu-id="7f61c-102">Greaterthanorequali-Funktion</span><span class="sxs-lookup"><span data-stu-id="7f61c-102">GreaterThanOrEqualI function</span></span>

<span data-ttu-id="7f61c-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="7f61c-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="7f61c-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7f61c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7f61c-105">Gibt nur dann true zurück, wenn eine Zahl größer als eine andere Zahl oder gleich einer anderen Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="7f61c-105">Returns true if and only if a number is greater than or equal to another number.</span></span>

```qsharp
function GreaterThanOrEqualI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="7f61c-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7f61c-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="7f61c-107">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7f61c-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="7f61c-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="7f61c-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="7f61c-109">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7f61c-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="7f61c-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="7f61c-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="7f61c-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="7f61c-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="7f61c-112">`true``a`, wenn größer als oder gleich ist `b` .</span><span class="sxs-lookup"><span data-stu-id="7f61c-112">`true` if and only if `a` is greater than or is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f61c-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7f61c-113">Remarks</span></span>

<span data-ttu-id="7f61c-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="7f61c-114">The following are equivalent:</span></span>

```Q#
let cond = a >= b;
let cond = GreaterThanOrEqualI(a, b);
```
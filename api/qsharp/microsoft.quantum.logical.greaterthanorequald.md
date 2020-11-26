---
uid: Microsoft.Quantum.Logical.GreaterThanOrEqualD
title: Greaterthanorequald-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanOrEqualD
qsharp.summary: Returns true if and only if a number is greater than or equal to another number.
ms.openlocfilehash: 0c9fa353b549d3c137beac3bcc3cfb0e742f6d07
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197805"
---
# <a name="greaterthanorequald-function"></a><span data-ttu-id="6acc9-102">Greaterthanorequald-Funktion</span><span class="sxs-lookup"><span data-stu-id="6acc9-102">GreaterThanOrEqualD function</span></span>

<span data-ttu-id="6acc9-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="6acc9-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="6acc9-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6acc9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6acc9-105">Gibt nur dann true zurück, wenn eine Zahl größer als eine andere Zahl oder gleich einer anderen Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="6acc9-105">Returns true if and only if a number is greater than or equal to another number.</span></span>

```qsharp
function GreaterThanOrEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="6acc9-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6acc9-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="6acc9-107">a: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="6acc9-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="6acc9-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="6acc9-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="6acc9-109">b: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="6acc9-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="6acc9-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="6acc9-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="6acc9-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="6acc9-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="6acc9-112">`true``a`, wenn größer als oder gleich ist `b` .</span><span class="sxs-lookup"><span data-stu-id="6acc9-112">`true` if and only if `a` is greater than or is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="6acc9-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6acc9-113">Remarks</span></span>

<span data-ttu-id="6acc9-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="6acc9-114">The following are equivalent:</span></span>

```Q#
let cond = a >= b;
let cond = GreaterThanOrEqualD(a, b);
```
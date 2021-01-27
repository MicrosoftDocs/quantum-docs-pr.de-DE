---
uid: Microsoft.Quantum.Logical.GreaterThanOrEqualI
title: Greaterthanorequali-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanOrEqualI
qsharp.summary: Returns true if and only if a number is greater than or equal to another number.
ms.openlocfilehash: c1a513500c8a70bd7628976974387cba48162e80
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849188"
---
# <a name="greaterthanorequali-function"></a><span data-ttu-id="df2c7-102">Greaterthanorequali-Funktion</span><span class="sxs-lookup"><span data-stu-id="df2c7-102">GreaterThanOrEqualI function</span></span>

<span data-ttu-id="df2c7-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="df2c7-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="df2c7-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="df2c7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="df2c7-105">Gibt nur dann true zurück, wenn eine Zahl größer als eine andere Zahl oder gleich einer anderen Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="df2c7-105">Returns true if and only if a number is greater than or equal to another number.</span></span>

```qsharp
function GreaterThanOrEqualI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="df2c7-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="df2c7-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="df2c7-107">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="df2c7-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="df2c7-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="df2c7-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="df2c7-109">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="df2c7-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="df2c7-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="df2c7-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="df2c7-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="df2c7-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="df2c7-112">`true``a`, wenn größer als oder gleich ist `b` .</span><span class="sxs-lookup"><span data-stu-id="df2c7-112">`true` if and only if `a` is greater than or is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="df2c7-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="df2c7-113">Remarks</span></span>

<span data-ttu-id="df2c7-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="df2c7-114">The following are equivalent:</span></span>

```qsharp
let cond = a >= b;
let cond = GreaterThanOrEqualI(a, b);
```
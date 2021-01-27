---
uid: Microsoft.Quantum.Logical.GreaterThanOrEqualD
title: Greaterthanorequald-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanOrEqualD
qsharp.summary: Returns true if and only if a number is greater than or equal to another number.
ms.openlocfilehash: 98fa55c249f2ade414254d1bccda46a8602b828c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98815863"
---
# <a name="greaterthanorequald-function"></a><span data-ttu-id="15f16-102">Greaterthanorequald-Funktion</span><span class="sxs-lookup"><span data-stu-id="15f16-102">GreaterThanOrEqualD function</span></span>

<span data-ttu-id="15f16-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="15f16-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="15f16-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="15f16-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="15f16-105">Gibt nur dann true zurück, wenn eine Zahl größer als eine andere Zahl oder gleich einer anderen Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="15f16-105">Returns true if and only if a number is greater than or equal to another number.</span></span>

```qsharp
function GreaterThanOrEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="15f16-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="15f16-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="15f16-107">a: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="15f16-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="15f16-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="15f16-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="15f16-109">b: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="15f16-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="15f16-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="15f16-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="15f16-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="15f16-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="15f16-112">`true``a`, wenn größer als oder gleich ist `b` .</span><span class="sxs-lookup"><span data-stu-id="15f16-112">`true` if and only if `a` is greater than or is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="15f16-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15f16-113">Remarks</span></span>

<span data-ttu-id="15f16-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="15f16-114">The following are equivalent:</span></span>

```qsharp
let cond = a >= b;
let cond = GreaterThanOrEqualD(a, b);
```
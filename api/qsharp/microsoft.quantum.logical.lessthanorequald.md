---
uid: Microsoft.Quantum.Logical.LessThanOrEqualD
title: Lessthanorequald-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanOrEqualD
qsharp.summary: Returns true if and only if a number is less than or equal to another number.
ms.openlocfilehash: 703b782efe9daccd4f6a339481d49ae9232123f3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849139"
---
# <a name="lessthanorequald-function"></a><span data-ttu-id="02646-102">Lessthanorequald-Funktion</span><span class="sxs-lookup"><span data-stu-id="02646-102">LessThanOrEqualD function</span></span>

<span data-ttu-id="02646-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="02646-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="02646-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="02646-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="02646-105">Gibt nur dann true zurück, wenn eine Zahl kleiner oder gleich einer anderen Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="02646-105">Returns true if and only if a number is less than or equal to another number.</span></span>

```qsharp
function LessThanOrEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="02646-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="02646-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="02646-107">a: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="02646-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="02646-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="02646-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="02646-109">b: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="02646-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="02646-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="02646-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="02646-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="02646-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="02646-112">`true``a`, wenn kleiner oder gleich ist `b` .</span><span class="sxs-lookup"><span data-stu-id="02646-112">`true` if and only if `a` is less than or equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="02646-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02646-113">Remarks</span></span>

<span data-ttu-id="02646-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="02646-114">The following are equivalent:</span></span>

```qsharp
let cond = a <= b;
let cond = LessThanOrEqualD(a, b);
```
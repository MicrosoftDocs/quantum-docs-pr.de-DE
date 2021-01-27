---
uid: Microsoft.Quantum.Logical.Or
title: Or-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Or
qsharp.summary: Returns the Boolean disjunction of two values.
ms.openlocfilehash: 4a29b7684b28b904b43ccceb8e63280999690349
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848465"
---
# <a name="or-function"></a><span data-ttu-id="39463-102">Or-Funktion</span><span class="sxs-lookup"><span data-stu-id="39463-102">Or function</span></span>

<span data-ttu-id="39463-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="39463-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="39463-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="39463-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="39463-105">Gibt die boolesche Disjunktion von zwei Werten zurück.</span><span class="sxs-lookup"><span data-stu-id="39463-105">Returns the Boolean disjunction of two values.</span></span>

```qsharp
function Or (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="39463-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="39463-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="39463-107">a: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="39463-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="39463-108">Der erste zu berücksichtigende Wert.</span><span class="sxs-lookup"><span data-stu-id="39463-108">The first value to be considered.</span></span>


### <a name="b--bool"></a><span data-ttu-id="39463-109">b: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="39463-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="39463-110">Der zweite zu berücksichtigende Wert.</span><span class="sxs-lookup"><span data-stu-id="39463-110">The second value to be considered.</span></span>



## <a name="output--bool"></a><span data-ttu-id="39463-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="39463-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="39463-112">`true` nur dann, wenn entweder `a` oder `b` ist `true` .</span><span class="sxs-lookup"><span data-stu-id="39463-112">`true` if and only if either `a` or `b` are `true`.</span></span>

## <a name="remarks"></a><span data-ttu-id="39463-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39463-113">Remarks</span></span>

<span data-ttu-id="39463-114">Im Gegensatz zum- `or` Operator ist diese Funktion nicht kurz, sodass beide Eingaben vollständig ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="39463-114">Unlike the `or` operator, this function does not short-circuit, such that both inputs are fully evaluated.</span></span>

<span data-ttu-id="39463-115">Bis zu einem kurzen Schluss Verhalten sind die folgenden äquivalent:</span><span class="sxs-lookup"><span data-stu-id="39463-115">Up to short-circuiting behavior, the following are equivalent:</span></span>

```qsharp
let x = a or b;
let x = Or(a, b);
```
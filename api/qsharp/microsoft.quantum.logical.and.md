---
uid: Microsoft.Quantum.Logical.And
title: And-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: And
qsharp.summary: Returns the Boolean conjunction of two values.
ms.openlocfilehash: 279221ed785dd76e28146e4c22e70290936bf529
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198570"
---
# <a name="and-function"></a><span data-ttu-id="0cc53-102">And-Funktion</span><span class="sxs-lookup"><span data-stu-id="0cc53-102">And function</span></span>

<span data-ttu-id="0cc53-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="0cc53-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="0cc53-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0cc53-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0cc53-105">Gibt die boolesche Verbindung von zwei Werten zurück.</span><span class="sxs-lookup"><span data-stu-id="0cc53-105">Returns the Boolean conjunction of two values.</span></span>

```qsharp
function And (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="0cc53-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0cc53-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="0cc53-107">a: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="0cc53-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="0cc53-108">Der erste zu berücksichtigende Wert.</span><span class="sxs-lookup"><span data-stu-id="0cc53-108">The first value to be considered.</span></span>


### <a name="b--bool"></a><span data-ttu-id="0cc53-109">b: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="0cc53-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="0cc53-110">Der zweite zu berücksichtigende Wert.</span><span class="sxs-lookup"><span data-stu-id="0cc53-110">The second value to be considered.</span></span>



## <a name="output--bool"></a><span data-ttu-id="0cc53-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="0cc53-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="0cc53-112">`true` nur dann, wenn `a` und gleich `b` sind `true` .</span><span class="sxs-lookup"><span data-stu-id="0cc53-112">`true` if and only if `a` and `b` are both `true`.</span></span>

## <a name="remarks"></a><span data-ttu-id="0cc53-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0cc53-113">Remarks</span></span>

<span data-ttu-id="0cc53-114">Im Gegensatz zum- `and` Operator ist diese Funktion nicht kurz, sodass beide Eingaben vollständig ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="0cc53-114">Unlike the `and` operator, this function does not short-circuit, such that both inputs are fully evaluated.</span></span>

<span data-ttu-id="0cc53-115">Bis zu einem kurzen Schluss Verhalten sind die folgenden äquivalent:</span><span class="sxs-lookup"><span data-stu-id="0cc53-115">Up to short-circuiting behavior, the following are equivalent:</span></span>

```Q#
let x = a and b;
let x = And(a, b);
```
---
uid: Microsoft.Quantum.Logical.And
title: And-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: And
qsharp.summary: Returns the Boolean conjunction of two values.
ms.openlocfilehash: 6c405bdb4182cc7f32bd04952dec25a974c03445
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849228"
---
# <a name="and-function"></a><span data-ttu-id="be9a4-102">And-Funktion</span><span class="sxs-lookup"><span data-stu-id="be9a4-102">And function</span></span>

<span data-ttu-id="be9a4-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="be9a4-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="be9a4-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="be9a4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="be9a4-105">Gibt die boolesche Verbindung von zwei Werten zurück.</span><span class="sxs-lookup"><span data-stu-id="be9a4-105">Returns the Boolean conjunction of two values.</span></span>

```qsharp
function And (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="be9a4-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="be9a4-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="be9a4-107">a: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="be9a4-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="be9a4-108">Der erste zu berücksichtigende Wert.</span><span class="sxs-lookup"><span data-stu-id="be9a4-108">The first value to be considered.</span></span>


### <a name="b--bool"></a><span data-ttu-id="be9a4-109">b: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="be9a4-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="be9a4-110">Der zweite zu berücksichtigende Wert.</span><span class="sxs-lookup"><span data-stu-id="be9a4-110">The second value to be considered.</span></span>



## <a name="output--bool"></a><span data-ttu-id="be9a4-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="be9a4-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="be9a4-112">`true` nur dann, wenn `a` und gleich `b` sind `true` .</span><span class="sxs-lookup"><span data-stu-id="be9a4-112">`true` if and only if `a` and `b` are both `true`.</span></span>

## <a name="remarks"></a><span data-ttu-id="be9a4-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="be9a4-113">Remarks</span></span>

<span data-ttu-id="be9a4-114">Im Gegensatz zum- `and` Operator ist diese Funktion nicht kurz, sodass beide Eingaben vollständig ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="be9a4-114">Unlike the `and` operator, this function does not short-circuit, such that both inputs are fully evaluated.</span></span>

<span data-ttu-id="be9a4-115">Bis zu einem kurzen Schluss Verhalten sind die folgenden äquivalent:</span><span class="sxs-lookup"><span data-stu-id="be9a4-115">Up to short-circuiting behavior, the following are equivalent:</span></span>

```qsharp
let x = a and b;
let x = And(a, b);
```
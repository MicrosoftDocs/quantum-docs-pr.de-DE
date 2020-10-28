---
uid: Microsoft.Quantum.Logical.And
title: And-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: And
qsharp.summary: Returns the Boolean conjunction of two values.
ms.openlocfilehash: cc81f650216c4db219a79c4fe89a42447a4e95b8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707063"
---
# <a name="and-function"></a><span data-ttu-id="69df8-102">And-Funktion</span><span class="sxs-lookup"><span data-stu-id="69df8-102">And function</span></span>

<span data-ttu-id="69df8-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="69df8-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="69df8-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="69df8-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="69df8-105">Gibt die boolesche Verbindung von zwei Werten zurück.</span><span class="sxs-lookup"><span data-stu-id="69df8-105">Returns the Boolean conjunction of two values.</span></span>

```qsharp
function And (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="69df8-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="69df8-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="69df8-107">a: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="69df8-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="69df8-108">Der erste zu berücksichtigende Wert.</span><span class="sxs-lookup"><span data-stu-id="69df8-108">The first value to be considered.</span></span>


### <a name="b--bool"></a><span data-ttu-id="69df8-109">b: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="69df8-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="69df8-110">Der zweite zu berücksichtigende Wert.</span><span class="sxs-lookup"><span data-stu-id="69df8-110">The second value to be considered.</span></span>



## <a name="output--bool"></a><span data-ttu-id="69df8-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="69df8-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="69df8-112">`true` nur dann, wenn `a` und gleich `b` sind `true` .</span><span class="sxs-lookup"><span data-stu-id="69df8-112">`true` if and only if `a` and `b` are both `true`.</span></span>

## <a name="remarks"></a><span data-ttu-id="69df8-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="69df8-113">Remarks</span></span>

<span data-ttu-id="69df8-114">Im Gegensatz zum- `and` Operator ist diese Funktion nicht kurz, sodass beide Eingaben vollständig ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="69df8-114">Unlike the `and` operator, this function does not short-circuit, such that both inputs are fully evaluated.</span></span>

<span data-ttu-id="69df8-115">Bis zu einem kurzen Schluss Verhalten sind die folgenden äquivalent:</span><span class="sxs-lookup"><span data-stu-id="69df8-115">Up to short-circuiting behavior, the following are equivalent:</span></span>

```Q#
let x = a and b;
let x = And(a, b);
```
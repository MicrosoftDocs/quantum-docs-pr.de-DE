---
uid: Microsoft.Quantum.Logical.EqualI
title: Equali-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualI
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: 87cf00ea8bb738cda30092b3d80940291beb1fb9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98816751"
---
# <a name="equali-function"></a><span data-ttu-id="b56e8-102">Equali-Funktion</span><span class="sxs-lookup"><span data-stu-id="b56e8-102">EqualI function</span></span>

<span data-ttu-id="b56e8-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="b56e8-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="b56e8-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b56e8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b56e8-105">Gibt nur dann true zurück, wenn zwei Eingaben gleich sind.</span><span class="sxs-lookup"><span data-stu-id="b56e8-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="b56e8-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b56e8-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="b56e8-107">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b56e8-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b56e8-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="b56e8-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="b56e8-109">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b56e8-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b56e8-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="b56e8-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="b56e8-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="b56e8-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="b56e8-112">`true``a`, wenn gleich ist `b` .</span><span class="sxs-lookup"><span data-stu-id="b56e8-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="b56e8-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b56e8-113">Remarks</span></span>

<span data-ttu-id="b56e8-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="b56e8-114">The following are equivalent:</span></span>

```qsharp
let cond = a == b;
let cond = EqualI(a, b);
```
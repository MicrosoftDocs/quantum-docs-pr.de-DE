---
uid: Microsoft.Quantum.Logical.EqualL
title: Equall-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualL
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: 395b8fedd3b3334939c2a4b5602ee19e0c6e34b0
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198111"
---
# <a name="equall-function"></a><span data-ttu-id="6a885-102">Equall-Funktion</span><span class="sxs-lookup"><span data-stu-id="6a885-102">EqualL function</span></span>

<span data-ttu-id="6a885-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="6a885-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="6a885-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6a885-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6a885-105">Gibt nur dann true zurück, wenn zwei Eingaben gleich sind.</span><span class="sxs-lookup"><span data-stu-id="6a885-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="6a885-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6a885-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="6a885-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="6a885-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="6a885-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="6a885-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="6a885-109">b: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="6a885-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="6a885-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="6a885-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="6a885-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="6a885-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="6a885-112">`true``a`, wenn gleich ist `b` .</span><span class="sxs-lookup"><span data-stu-id="6a885-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a885-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6a885-113">Remarks</span></span>

<span data-ttu-id="6a885-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="6a885-114">The following are equivalent:</span></span>

```Q#
let cond = a == b;
let cond = EqualL(a, b);
```
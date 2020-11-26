---
uid: Microsoft.Quantum.Logical.LessThanL
title: Lessthanl-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanL
qsharp.summary: Returns true if and only if a number is less than another number.
ms.openlocfilehash: 9a0678569596ac188c87c3944f3759783fcc77ee
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197720"
---
# <a name="lessthanl-function"></a><span data-ttu-id="d9dfe-102">Lessthanl-Funktion</span><span class="sxs-lookup"><span data-stu-id="d9dfe-102">LessThanL function</span></span>

<span data-ttu-id="d9dfe-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="d9dfe-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="d9dfe-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d9dfe-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d9dfe-105">Gibt nur dann true zurück, wenn eine Zahl kleiner als eine andere Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="d9dfe-105">Returns true if and only if a number is less than another number.</span></span>

```qsharp
function LessThanL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="d9dfe-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d9dfe-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="d9dfe-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="d9dfe-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="d9dfe-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="d9dfe-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="d9dfe-109">b: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="d9dfe-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="d9dfe-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="d9dfe-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="d9dfe-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="d9dfe-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="d9dfe-112">`true` , wenn und nur, wenn `a` streng kleiner als ist `b` .</span><span class="sxs-lookup"><span data-stu-id="d9dfe-112">`true` if and only if `a` is strictly less than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9dfe-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d9dfe-113">Remarks</span></span>

<span data-ttu-id="d9dfe-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="d9dfe-114">The following are equivalent:</span></span>

```Q#
let cond = a < b;
let cond = LessThanL(a, b);
```
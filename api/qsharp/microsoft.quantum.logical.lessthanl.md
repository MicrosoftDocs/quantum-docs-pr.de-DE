---
uid: Microsoft.Quantum.Logical.LessThanL
title: Lessthanl-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanL
qsharp.summary: Returns true if and only if a number is less than another number.
ms.openlocfilehash: d5753f9e1447fc1bd433703037fe44c86aaa659c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849147"
---
# <a name="lessthanl-function"></a><span data-ttu-id="d1af9-102">Lessthanl-Funktion</span><span class="sxs-lookup"><span data-stu-id="d1af9-102">LessThanL function</span></span>

<span data-ttu-id="d1af9-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="d1af9-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="d1af9-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d1af9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d1af9-105">Gibt nur dann true zurück, wenn eine Zahl kleiner als eine andere Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="d1af9-105">Returns true if and only if a number is less than another number.</span></span>

```qsharp
function LessThanL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="d1af9-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d1af9-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="d1af9-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="d1af9-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="d1af9-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="d1af9-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="d1af9-109">b: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="d1af9-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="d1af9-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="d1af9-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="d1af9-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="d1af9-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="d1af9-112">`true` , wenn und nur, wenn `a` streng kleiner als ist `b` .</span><span class="sxs-lookup"><span data-stu-id="d1af9-112">`true` if and only if `a` is strictly less than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1af9-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d1af9-113">Remarks</span></span>

<span data-ttu-id="d1af9-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="d1af9-114">The following are equivalent:</span></span>

```qsharp
let cond = a < b;
let cond = LessThanL(a, b);
```
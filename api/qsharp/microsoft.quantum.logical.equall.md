---
uid: Microsoft.Quantum.Logical.EqualL
title: Equall-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualL
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: 58086f40ea20b6f1a5fa6996e3a6703e2bf66306
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98815964"
---
# <a name="equall-function"></a><span data-ttu-id="f4c65-102">Equall-Funktion</span><span class="sxs-lookup"><span data-stu-id="f4c65-102">EqualL function</span></span>

<span data-ttu-id="f4c65-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="f4c65-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="f4c65-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f4c65-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f4c65-105">Gibt nur dann true zurück, wenn zwei Eingaben gleich sind.</span><span class="sxs-lookup"><span data-stu-id="f4c65-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="f4c65-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f4c65-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="f4c65-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="f4c65-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="f4c65-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="f4c65-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="f4c65-109">b: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="f4c65-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="f4c65-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="f4c65-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="f4c65-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="f4c65-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="f4c65-112">`true``a`, wenn gleich ist `b` .</span><span class="sxs-lookup"><span data-stu-id="f4c65-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4c65-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f4c65-113">Remarks</span></span>

<span data-ttu-id="f4c65-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="f4c65-114">The following are equivalent:</span></span>

```qsharp
let cond = a == b;
let cond = EqualL(a, b);
```
---
uid: Microsoft.Quantum.Logical.GreaterThanOrEqualL
title: Greaterthanorequall-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanOrEqualL
qsharp.summary: Returns true if and only if a number is greater than or equal to another number.
ms.openlocfilehash: 5536c009d6e78eac9ab2320b42aec7d2d82946eb
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197754"
---
# <a name="greaterthanorequall-function"></a><span data-ttu-id="130dd-102">Greaterthanorequall-Funktion</span><span class="sxs-lookup"><span data-stu-id="130dd-102">GreaterThanOrEqualL function</span></span>

<span data-ttu-id="130dd-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="130dd-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="130dd-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="130dd-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="130dd-105">Gibt nur dann true zurück, wenn eine Zahl größer als eine andere Zahl oder gleich einer anderen Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="130dd-105">Returns true if and only if a number is greater than or equal to another number.</span></span>

```qsharp
function GreaterThanOrEqualL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="130dd-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="130dd-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="130dd-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="130dd-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="130dd-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="130dd-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="130dd-109">b: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="130dd-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="130dd-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="130dd-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="130dd-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="130dd-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="130dd-112">`true``a`, wenn größer als oder gleich ist `b` .</span><span class="sxs-lookup"><span data-stu-id="130dd-112">`true` if and only if `a` is greater than or is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="130dd-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="130dd-113">Remarks</span></span>

<span data-ttu-id="130dd-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="130dd-114">The following are equivalent:</span></span>

```Q#
let cond = a >= b;
let cond = GreaterThanOrEqualL(a, b);
```
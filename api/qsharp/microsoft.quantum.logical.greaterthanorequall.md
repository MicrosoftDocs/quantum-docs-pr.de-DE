---
uid: Microsoft.Quantum.Logical.GreaterThanOrEqualL
title: Greaterthanorequall-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanOrEqualL
qsharp.summary: Returns true if and only if a number is greater than or equal to another number.
ms.openlocfilehash: a59a9eca2941a44a70ec5a379b146ac459390bd4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722640"
---
# <a name="greaterthanorequall-function"></a><span data-ttu-id="93cab-102">Greaterthanorequall-Funktion</span><span class="sxs-lookup"><span data-stu-id="93cab-102">GreaterThanOrEqualL function</span></span>

<span data-ttu-id="93cab-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="93cab-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="93cab-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="93cab-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="93cab-105">Gibt nur dann true zurück, wenn eine Zahl größer als eine andere Zahl oder gleich einer anderen Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="93cab-105">Returns true if and only if a number is greater than or equal to another number.</span></span>

```qsharp
function GreaterThanOrEqualL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="93cab-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="93cab-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="93cab-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="93cab-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="93cab-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="93cab-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="93cab-109">b: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="93cab-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="93cab-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="93cab-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="93cab-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="93cab-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="93cab-112">`true``a`, wenn größer als oder gleich ist `b` .</span><span class="sxs-lookup"><span data-stu-id="93cab-112">`true` if and only if `a` is greater than or is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="93cab-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="93cab-113">Remarks</span></span>

<span data-ttu-id="93cab-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="93cab-114">The following are equivalent:</span></span>

```Q#
let cond = a >= b;
let cond = GreaterThanOrEqualL(a, b);
```
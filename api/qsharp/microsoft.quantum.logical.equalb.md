---
uid: Microsoft.Quantum.Logical.EqualB
title: Equalb-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualB
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: b566f5ba8548eadeecf63a1e91956d936e7e9a20
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198468"
---
# <a name="equalb-function"></a><span data-ttu-id="cc52e-102">Equalb-Funktion</span><span class="sxs-lookup"><span data-stu-id="cc52e-102">EqualB function</span></span>

<span data-ttu-id="cc52e-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="cc52e-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="cc52e-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cc52e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cc52e-105">Gibt nur dann true zurück, wenn zwei Eingaben gleich sind.</span><span class="sxs-lookup"><span data-stu-id="cc52e-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualB (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="cc52e-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cc52e-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="cc52e-107">a: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="cc52e-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="cc52e-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="cc52e-108">The first value to be compared.</span></span>


### <a name="b--bool"></a><span data-ttu-id="cc52e-109">b: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="cc52e-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="cc52e-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="cc52e-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="cc52e-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="cc52e-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="cc52e-112">`true``a`, wenn gleich ist `b` .</span><span class="sxs-lookup"><span data-stu-id="cc52e-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc52e-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cc52e-113">Remarks</span></span>

<span data-ttu-id="cc52e-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="cc52e-114">The following are equivalent:</span></span>

```Q#
let cond = a == b;
let cond = EqualB(a, b);
```
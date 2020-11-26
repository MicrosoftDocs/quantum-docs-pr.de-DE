---
uid: Microsoft.Quantum.Logical.EqualD
title: Equald-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualD
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: d6731b293ba402f5cd43591d3c2bcd258e8ebe32
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198145"
---
# <a name="equald-function"></a><span data-ttu-id="48533-102">Equald-Funktion</span><span class="sxs-lookup"><span data-stu-id="48533-102">EqualD function</span></span>

<span data-ttu-id="48533-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="48533-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="48533-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="48533-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="48533-105">Gibt nur dann true zurück, wenn zwei Eingaben gleich sind.</span><span class="sxs-lookup"><span data-stu-id="48533-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="48533-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="48533-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="48533-107">a: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="48533-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="48533-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="48533-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="48533-109">b: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="48533-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="48533-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="48533-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="48533-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="48533-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="48533-112">`true``a`, wenn gleich ist `b` .</span><span class="sxs-lookup"><span data-stu-id="48533-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="48533-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="48533-113">Remarks</span></span>

<span data-ttu-id="48533-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="48533-114">The following are equivalent:</span></span>

```Q#
let cond = a == b;
let cond = EqualD(a, b);
```
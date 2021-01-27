---
uid: Microsoft.Quantum.Logical.EqualD
title: Equald-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualD
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: f8a24d7bfb9b4f7b8b0e1f68a94bfb341716b024
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98816869"
---
# <a name="equald-function"></a><span data-ttu-id="56252-102">Equald-Funktion</span><span class="sxs-lookup"><span data-stu-id="56252-102">EqualD function</span></span>

<span data-ttu-id="56252-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="56252-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="56252-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="56252-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="56252-105">Gibt nur dann true zurück, wenn zwei Eingaben gleich sind.</span><span class="sxs-lookup"><span data-stu-id="56252-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="56252-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="56252-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="56252-107">a: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="56252-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="56252-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="56252-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="56252-109">b: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="56252-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="56252-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="56252-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="56252-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="56252-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="56252-112">`true``a`, wenn gleich ist `b` .</span><span class="sxs-lookup"><span data-stu-id="56252-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="56252-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="56252-113">Remarks</span></span>

<span data-ttu-id="56252-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="56252-114">The following are equivalent:</span></span>

```qsharp
let cond = a == b;
let cond = EqualD(a, b);
```
---
uid: Microsoft.Quantum.Logical.EqualB
title: Equalb-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualB
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: 91ab51180018a9b95a2f9010477c0a24f3a54617
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707050"
---
# <a name="equalb-function"></a><span data-ttu-id="d0262-102">Equalb-Funktion</span><span class="sxs-lookup"><span data-stu-id="d0262-102">EqualB function</span></span>

<span data-ttu-id="d0262-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="d0262-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="d0262-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d0262-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d0262-105">Gibt nur dann true zurück, wenn zwei Eingaben gleich sind.</span><span class="sxs-lookup"><span data-stu-id="d0262-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualB (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="d0262-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d0262-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="d0262-107">a: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="d0262-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="d0262-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="d0262-108">The first value to be compared.</span></span>


### <a name="b--bool"></a><span data-ttu-id="d0262-109">b: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="d0262-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="d0262-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="d0262-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="d0262-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="d0262-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="d0262-112">`true``a`, wenn gleich ist `b` .</span><span class="sxs-lookup"><span data-stu-id="d0262-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0262-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d0262-113">Remarks</span></span>

<span data-ttu-id="d0262-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="d0262-114">The following are equivalent:</span></span>

```Q#
let cond = a == b;
let cond = EqualB(a, b);
```
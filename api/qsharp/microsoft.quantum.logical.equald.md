---
uid: Microsoft.Quantum.Logical.EqualD
title: Equald-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualD
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: 024ddee785a6a907b4a39d0eccc5990b4c5d5d83
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702078"
---
# <a name="equald-function"></a><span data-ttu-id="5f911-102">Equald-Funktion</span><span class="sxs-lookup"><span data-stu-id="5f911-102">EqualD function</span></span>

<span data-ttu-id="5f911-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="5f911-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="5f911-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5f911-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5f911-105">Gibt nur dann true zurück, wenn zwei Eingaben gleich sind.</span><span class="sxs-lookup"><span data-stu-id="5f911-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="5f911-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5f911-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="5f911-107">a: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="5f911-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="5f911-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="5f911-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="5f911-109">b: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="5f911-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="5f911-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="5f911-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="5f911-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="5f911-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="5f911-112">`true``a`, wenn gleich ist `b` .</span><span class="sxs-lookup"><span data-stu-id="5f911-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f911-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5f911-113">Remarks</span></span>

<span data-ttu-id="5f911-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="5f911-114">The following are equivalent:</span></span>

```Q#
let cond = a == b;
let cond = EqualD(a, b);
```
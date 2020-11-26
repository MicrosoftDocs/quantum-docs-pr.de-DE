---
uid: Microsoft.Quantum.Logical.NotEqualD
title: Notequald-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualD
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: 4599d7125dbc67547af454183f620e8d84f2caf7
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197244"
---
# <a name="notequald-function"></a><span data-ttu-id="86be4-102">Notequald-Funktion</span><span class="sxs-lookup"><span data-stu-id="86be4-102">NotEqualD function</span></span>

<span data-ttu-id="86be4-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="86be4-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="86be4-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="86be4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="86be4-105">Gibt nur dann true zurück, wenn zwei Eingaben nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="86be4-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="86be4-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="86be4-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="86be4-107">a: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="86be4-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="86be4-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="86be4-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="86be4-109">b: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="86be4-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="86be4-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="86be4-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="86be4-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="86be4-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="86be4-112">`true``a`, wenn nicht gleich ist `b` .</span><span class="sxs-lookup"><span data-stu-id="86be4-112">`true` if and only if `a` is not equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="86be4-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="86be4-113">Remarks</span></span>

<span data-ttu-id="86be4-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="86be4-114">The following are equivalent:</span></span>

```Q#
let cond = a != b;
let cond = NotEqualD(a, b);
```
---
uid: Microsoft.Quantum.Logical.NotEqualI
title: Notequali-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualI
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: f88ae08f45c284f65151419c214705c74c3fadac
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98814503"
---
# <a name="notequali-function"></a><span data-ttu-id="50cd4-102">Notequali-Funktion</span><span class="sxs-lookup"><span data-stu-id="50cd4-102">NotEqualI function</span></span>

<span data-ttu-id="50cd4-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="50cd4-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="50cd4-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="50cd4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="50cd4-105">Gibt nur dann true zurück, wenn zwei Eingaben nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="50cd4-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="50cd4-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="50cd4-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="50cd4-107">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="50cd4-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="50cd4-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="50cd4-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="50cd4-109">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="50cd4-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="50cd4-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="50cd4-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="50cd4-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="50cd4-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="50cd4-112">`true``a`, wenn nicht gleich ist `b` .</span><span class="sxs-lookup"><span data-stu-id="50cd4-112">`true` if and only if `a` is not equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="50cd4-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50cd4-113">Remarks</span></span>

<span data-ttu-id="50cd4-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="50cd4-114">The following are equivalent:</span></span>

```qsharp
let cond = a != b;
let cond = NotEqualI(a, b);
```
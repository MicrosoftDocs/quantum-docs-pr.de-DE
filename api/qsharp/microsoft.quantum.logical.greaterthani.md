---
uid: Microsoft.Quantum.Logical.GreaterThanI
title: Greaterthani-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanI
qsharp.summary: Returns true if and only if a number is greater than another number.
ms.openlocfilehash: 86fc8e927c292a2ea814ed80a33de42bffdb96b1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98815954"
---
# <a name="greaterthani-function"></a><span data-ttu-id="2c5f8-102">Greaterthani-Funktion</span><span class="sxs-lookup"><span data-stu-id="2c5f8-102">GreaterThanI function</span></span>

<span data-ttu-id="2c5f8-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="2c5f8-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="2c5f8-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2c5f8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2c5f8-105">Gibt nur dann true zurück, wenn eine Zahl größer als eine andere Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="2c5f8-105">Returns true if and only if a number is greater than another number.</span></span>

```qsharp
function GreaterThanI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="2c5f8-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2c5f8-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="2c5f8-107">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2c5f8-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2c5f8-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="2c5f8-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="2c5f8-109">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2c5f8-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2c5f8-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="2c5f8-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="2c5f8-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="2c5f8-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="2c5f8-112">`true` , wenn und nur, wenn `a` streng größer als ist `b` .</span><span class="sxs-lookup"><span data-stu-id="2c5f8-112">`true` if and only if `a` is strictly greater than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c5f8-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2c5f8-113">Remarks</span></span>

<span data-ttu-id="2c5f8-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="2c5f8-114">The following are equivalent:</span></span>

```qsharp
let cond = a > b;
let cond = GreaterThanI(a, b);
```
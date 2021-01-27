---
uid: Microsoft.Quantum.Logical.EqualB
title: Equalb-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualB
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: 2a15a749f52fe814db4fa57118f69c80fa22158a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98817256"
---
# <a name="equalb-function"></a><span data-ttu-id="94b23-102">Equalb-Funktion</span><span class="sxs-lookup"><span data-stu-id="94b23-102">EqualB function</span></span>

<span data-ttu-id="94b23-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="94b23-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="94b23-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="94b23-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="94b23-105">Gibt nur dann true zurück, wenn zwei Eingaben gleich sind.</span><span class="sxs-lookup"><span data-stu-id="94b23-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualB (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="94b23-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="94b23-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="94b23-107">a: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="94b23-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="94b23-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="94b23-108">The first value to be compared.</span></span>


### <a name="b--bool"></a><span data-ttu-id="94b23-109">b: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="94b23-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="94b23-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="94b23-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="94b23-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="94b23-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="94b23-112">`true``a`, wenn gleich ist `b` .</span><span class="sxs-lookup"><span data-stu-id="94b23-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="94b23-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="94b23-113">Remarks</span></span>

<span data-ttu-id="94b23-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="94b23-114">The following are equivalent:</span></span>

```qsharp
let cond = a == b;
let cond = EqualB(a, b);
```
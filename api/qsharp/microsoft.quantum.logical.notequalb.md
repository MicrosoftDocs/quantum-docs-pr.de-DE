---
uid: Microsoft.Quantum.Logical.NotEqualB
title: Notequalb-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualB
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: d5a9819bf3baa7c914487277fef308abbc8d25bd
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701411"
---
# <a name="notequalb-function"></a><span data-ttu-id="02888-102">Notequalb-Funktion</span><span class="sxs-lookup"><span data-stu-id="02888-102">NotEqualB function</span></span>

<span data-ttu-id="02888-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="02888-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="02888-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="02888-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="02888-105">Gibt nur dann true zurück, wenn zwei Eingaben nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="02888-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualB (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="02888-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="02888-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="02888-107">a: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="02888-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="02888-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="02888-108">The first value to be compared.</span></span>


### <a name="b--bool"></a><span data-ttu-id="02888-109">b: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="02888-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="02888-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="02888-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="02888-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="02888-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="02888-112">`true``a`, wenn nicht gleich ist `b` .</span><span class="sxs-lookup"><span data-stu-id="02888-112">`true` if and only if `a` is not equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="02888-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="02888-113">Remarks</span></span>

<span data-ttu-id="02888-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="02888-114">The following are equivalent:</span></span>

```Q#
let cond = a != b;
let cond = NotEqualB(a, b);
```
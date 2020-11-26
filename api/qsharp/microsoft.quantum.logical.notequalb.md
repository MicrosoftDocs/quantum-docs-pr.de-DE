---
uid: Microsoft.Quantum.Logical.NotEqualB
title: Notequalb-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualB
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: 7943411b662683df058213a9e4b8eb7c9329ff07
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197380"
---
# <a name="notequalb-function"></a><span data-ttu-id="f370c-102">Notequalb-Funktion</span><span class="sxs-lookup"><span data-stu-id="f370c-102">NotEqualB function</span></span>

<span data-ttu-id="f370c-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="f370c-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="f370c-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f370c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f370c-105">Gibt nur dann true zurück, wenn zwei Eingaben nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="f370c-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualB (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="f370c-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f370c-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="f370c-107">a: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="f370c-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="f370c-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="f370c-108">The first value to be compared.</span></span>


### <a name="b--bool"></a><span data-ttu-id="f370c-109">b: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="f370c-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="f370c-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="f370c-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="f370c-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="f370c-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="f370c-112">`true``a`, wenn nicht gleich ist `b` .</span><span class="sxs-lookup"><span data-stu-id="f370c-112">`true` if and only if `a` is not equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="f370c-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f370c-113">Remarks</span></span>

<span data-ttu-id="f370c-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="f370c-114">The following are equivalent:</span></span>

```Q#
let cond = a != b;
let cond = NotEqualB(a, b);
```
---
uid: Microsoft.Quantum.Logical.NotEqualC
title: Notequalc-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualC
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: 33049b09405529bd418ff8652b6cb0f11bf734f0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849067"
---
# <a name="notequalc-function"></a><span data-ttu-id="e99b5-102">Notequalc-Funktion</span><span class="sxs-lookup"><span data-stu-id="e99b5-102">NotEqualC function</span></span>

<span data-ttu-id="e99b5-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="e99b5-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="e99b5-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e99b5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e99b5-105">Gibt nur dann true zurück, wenn zwei Eingaben nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="e99b5-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualC (a : Microsoft.Quantum.Math.Complex, b : Microsoft.Quantum.Math.Complex) : Bool
```


## <a name="input"></a><span data-ttu-id="e99b5-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e99b5-106">Input</span></span>

### <a name="a--complex"></a><span data-ttu-id="e99b5-107">a: [Komplex](xref:Microsoft.Quantum.Math.Complex)</span><span class="sxs-lookup"><span data-stu-id="e99b5-107">a : [Complex](xref:Microsoft.Quantum.Math.Complex)</span></span>

<span data-ttu-id="e99b5-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="e99b5-108">The first value to be compared.</span></span>


### <a name="b--complex"></a><span data-ttu-id="e99b5-109">b: [Komplex](xref:Microsoft.Quantum.Math.Complex)</span><span class="sxs-lookup"><span data-stu-id="e99b5-109">b : [Complex](xref:Microsoft.Quantum.Math.Complex)</span></span>

<span data-ttu-id="e99b5-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="e99b5-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="e99b5-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="e99b5-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="e99b5-112">`true``a`, wenn nicht gleich ist `b` .</span><span class="sxs-lookup"><span data-stu-id="e99b5-112">`true` if and only if `a` is not equal to `b`.</span></span>
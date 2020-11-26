---
uid: Microsoft.Quantum.Logical.EqualCP
title: Equalcp-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualCP
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: e3175b9b6fd2890963de0452102e2f0de1026b91
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198230"
---
# <a name="equalcp-function"></a><span data-ttu-id="c8c40-102">Equalcp-Funktion</span><span class="sxs-lookup"><span data-stu-id="c8c40-102">EqualCP function</span></span>

<span data-ttu-id="c8c40-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="c8c40-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="c8c40-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c8c40-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c8c40-105">Gibt nur dann true zurück, wenn zwei Eingaben gleich sind.</span><span class="sxs-lookup"><span data-stu-id="c8c40-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualCP (a : Microsoft.Quantum.Math.ComplexPolar, b : Microsoft.Quantum.Math.ComplexPolar) : Bool
```


## <a name="input"></a><span data-ttu-id="c8c40-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c8c40-106">Input</span></span>

### <a name="a--complexpolar"></a><span data-ttu-id="c8c40-107">a: [complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="c8c40-107">a : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="c8c40-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="c8c40-108">The first value to be compared.</span></span>


### <a name="b--complexpolar"></a><span data-ttu-id="c8c40-109">b: [complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="c8c40-109">b : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="c8c40-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="c8c40-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="c8c40-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="c8c40-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="c8c40-112">`true``a`, wenn gleich ist `b` .</span><span class="sxs-lookup"><span data-stu-id="c8c40-112">`true` if and only if `a` is equal to `b`.</span></span>
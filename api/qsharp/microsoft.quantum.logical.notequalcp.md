---
uid: Microsoft.Quantum.Logical.NotEqualCP
title: Notequalcp-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualCP
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: 81dd998353f674d55afe85dd20904047391bdb40
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707023"
---
# <a name="notequalcp-function"></a><span data-ttu-id="a3d83-102">Notequalcp-Funktion</span><span class="sxs-lookup"><span data-stu-id="a3d83-102">NotEqualCP function</span></span>

<span data-ttu-id="a3d83-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="a3d83-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="a3d83-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a3d83-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a3d83-105">Gibt nur dann true zurück, wenn zwei Eingaben nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="a3d83-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualCP (a : Microsoft.Quantum.Math.ComplexPolar, b : Microsoft.Quantum.Math.ComplexPolar) : Bool
```


## <a name="input"></a><span data-ttu-id="a3d83-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a3d83-106">Input</span></span>

### <a name="a--complexpolar"></a><span data-ttu-id="a3d83-107">a: [complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="a3d83-107">a : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="a3d83-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="a3d83-108">The first value to be compared.</span></span>


### <a name="b--complexpolar"></a><span data-ttu-id="a3d83-109">b: [complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="a3d83-109">b : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="a3d83-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="a3d83-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="a3d83-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="a3d83-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="a3d83-112">`true``a`, wenn nicht gleich ist `b` .</span><span class="sxs-lookup"><span data-stu-id="a3d83-112">`true` if and only if `a` is not equal to `b`.</span></span>
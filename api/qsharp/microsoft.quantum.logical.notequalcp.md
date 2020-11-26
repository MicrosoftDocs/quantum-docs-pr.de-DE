---
uid: Microsoft.Quantum.Logical.NotEqualCP
title: Notequalcp-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualCP
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: df735408f76eb6b88f0d867021d69b83edd69b7d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197295"
---
# <a name="notequalcp-function"></a><span data-ttu-id="ac41f-102">Notequalcp-Funktion</span><span class="sxs-lookup"><span data-stu-id="ac41f-102">NotEqualCP function</span></span>

<span data-ttu-id="ac41f-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="ac41f-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="ac41f-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ac41f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ac41f-105">Gibt nur dann true zurück, wenn zwei Eingaben nicht gleich sind.</span><span class="sxs-lookup"><span data-stu-id="ac41f-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualCP (a : Microsoft.Quantum.Math.ComplexPolar, b : Microsoft.Quantum.Math.ComplexPolar) : Bool
```


## <a name="input"></a><span data-ttu-id="ac41f-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ac41f-106">Input</span></span>

### <a name="a--complexpolar"></a><span data-ttu-id="ac41f-107">a: [complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="ac41f-107">a : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="ac41f-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="ac41f-108">The first value to be compared.</span></span>


### <a name="b--complexpolar"></a><span data-ttu-id="ac41f-109">b: [complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="ac41f-109">b : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="ac41f-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="ac41f-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="ac41f-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="ac41f-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="ac41f-112">`true``a`, wenn nicht gleich ist `b` .</span><span class="sxs-lookup"><span data-stu-id="ac41f-112">`true` if and only if `a` is not equal to `b`.</span></span>
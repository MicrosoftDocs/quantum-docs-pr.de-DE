---
uid: Microsoft.Quantum.Logical.EqualCP
title: Equalcp-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualCP
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: 83bf5ba245038ad1c7c6ed4e8cdb493317276e6a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98817160"
---
# <a name="equalcp-function"></a><span data-ttu-id="ecf3a-102">Equalcp-Funktion</span><span class="sxs-lookup"><span data-stu-id="ecf3a-102">EqualCP function</span></span>

<span data-ttu-id="ecf3a-103">Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="ecf3a-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="ecf3a-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ecf3a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ecf3a-105">Gibt nur dann true zurück, wenn zwei Eingaben gleich sind.</span><span class="sxs-lookup"><span data-stu-id="ecf3a-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualCP (a : Microsoft.Quantum.Math.ComplexPolar, b : Microsoft.Quantum.Math.ComplexPolar) : Bool
```


## <a name="input"></a><span data-ttu-id="ecf3a-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ecf3a-106">Input</span></span>

### <a name="a--complexpolar"></a><span data-ttu-id="ecf3a-107">a: [complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="ecf3a-107">a : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="ecf3a-108">Der erste zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="ecf3a-108">The first value to be compared.</span></span>


### <a name="b--complexpolar"></a><span data-ttu-id="ecf3a-109">b: [complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span><span class="sxs-lookup"><span data-stu-id="ecf3a-109">b : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)</span></span>

<span data-ttu-id="ecf3a-110">Der zweite zu vergleichende Wert.</span><span class="sxs-lookup"><span data-stu-id="ecf3a-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="ecf3a-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="ecf3a-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="ecf3a-112">`true``a`, wenn gleich ist `b` .</span><span class="sxs-lookup"><span data-stu-id="ecf3a-112">`true` if and only if `a` is equal to `b`.</span></span>
---
uid: Microsoft.Quantum.Canon.TrotterStepSize
title: Trotterstepsize-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TrotterStepSize
qsharp.summary: Computes Trotter step size in recursive implementation of Trotter simulation algorithm.
ms.openlocfilehash: aa5b63e058e1ea726b0d4c6eca73078831daaf3b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204690"
---
# <a name="trotterstepsize-function"></a><span data-ttu-id="8626e-102">Trotterstepsize-Funktion</span><span class="sxs-lookup"><span data-stu-id="8626e-102">TrotterStepSize function</span></span>

<span data-ttu-id="8626e-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="8626e-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="8626e-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8626e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8626e-105">Berechnet die Schrittgröße des Trotters in der rekursiven Implementierung des trocksimulations Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="8626e-105">Computes Trotter step size in recursive implementation of Trotter simulation algorithm.</span></span>

```qsharp
function TrotterStepSize (order : Int) : Double
```


## <a name="input"></a><span data-ttu-id="8626e-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8626e-106">Input</span></span>

### <a name="order--int"></a><span data-ttu-id="8626e-107">Reihenfolge: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8626e-107">order : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--double"></a><span data-ttu-id="8626e-108">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="8626e-108">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="remarks"></a><span data-ttu-id="8626e-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8626e-109">Remarks</span></span>

<span data-ttu-id="8626e-110">Bei diesem Vorgang wird eine andere Indizierungs Konvention verwendet als [quant-ph/0508139](https://arxiv.org/abs/quant-ph/0508139).</span><span class="sxs-lookup"><span data-stu-id="8626e-110">This operation uses a different indexing convention than that of [quant-ph/0508139](https://arxiv.org/abs/quant-ph/0508139).</span></span> <span data-ttu-id="8626e-111">Dies entspricht insbesondere `DecomposedIntoTimeStepsCA(_, 4)` dem skalaren $p _2 (\lambda) $ in quant-ph/0508139.</span><span class="sxs-lookup"><span data-stu-id="8626e-111">In particular, `DecomposedIntoTimeStepsCA(_, 4)` corresponds to the scalar $p_2(\lambda)$ in quant-ph/0508139.</span></span>
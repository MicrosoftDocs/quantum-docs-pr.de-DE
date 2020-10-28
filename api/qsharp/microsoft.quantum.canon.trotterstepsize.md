---
uid: Microsoft.Quantum.Canon.TrotterStepSize
title: Trotterstepsize-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TrotterStepSize
qsharp.summary: Computes Trotter step size in recursive implementation of Trotter simulation algorithm.
ms.openlocfilehash: fabfbff74572b3c96c701de5443e4265a0468d78
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703721"
---
# <a name="trotterstepsize-function"></a><span data-ttu-id="4abae-102">Trotterstepsize-Funktion</span><span class="sxs-lookup"><span data-stu-id="4abae-102">TrotterStepSize function</span></span>

<span data-ttu-id="4abae-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="4abae-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="4abae-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4abae-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4abae-105">Berechnet die Schrittgröße des Trotters in der rekursiven Implementierung des trocksimulations Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="4abae-105">Computes Trotter step size in recursive implementation of Trotter simulation algorithm.</span></span>

```qsharp
function TrotterStepSize (order : Int) : Double
```


## <a name="input"></a><span data-ttu-id="4abae-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4abae-106">Input</span></span>

### <a name="order--int"></a><span data-ttu-id="4abae-107">Reihenfolge: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4abae-107">order : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--double"></a><span data-ttu-id="4abae-108">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="4abae-108">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="remarks"></a><span data-ttu-id="4abae-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4abae-109">Remarks</span></span>

<span data-ttu-id="4abae-110">Bei diesem Vorgang wird eine andere Indizierungs Konvention verwendet als [quant-ph/0508139](https://arxiv.org/abs/quant-ph/0508139).</span><span class="sxs-lookup"><span data-stu-id="4abae-110">This operation uses a different indexing convention than that of [quant-ph/0508139](https://arxiv.org/abs/quant-ph/0508139).</span></span> <span data-ttu-id="4abae-111">Dies entspricht insbesondere `DecomposedIntoTimeStepsCA(_, 4)` dem skalaren $p _2 (\lambda) $ in quant-ph/0508139.</span><span class="sxs-lookup"><span data-stu-id="4abae-111">In particular, `DecomposedIntoTimeStepsCA(_, 4)` corresponds to the scalar $p_2(\lambda)$ in quant-ph/0508139.</span></span>
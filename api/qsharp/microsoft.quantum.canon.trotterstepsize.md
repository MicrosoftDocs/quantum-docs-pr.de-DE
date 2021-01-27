---
uid: Microsoft.Quantum.Canon.TrotterStepSize
title: Trotterstepsize-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TrotterStepSize
qsharp.summary: Computes Trotter step size in recursive implementation of Trotter simulation algorithm.
ms.openlocfilehash: c7b6432645dcad2bd47c62b91e04e0b42cd04ca9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840073"
---
# <a name="trotterstepsize-function"></a><span data-ttu-id="b4255-102">Trotterstepsize-Funktion</span><span class="sxs-lookup"><span data-stu-id="b4255-102">TrotterStepSize function</span></span>

<span data-ttu-id="b4255-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="b4255-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="b4255-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b4255-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b4255-105">Berechnet die Schrittgröße des Trotters in der rekursiven Implementierung des trocksimulations Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="b4255-105">Computes Trotter step size in recursive implementation of Trotter simulation algorithm.</span></span>

```qsharp
function TrotterStepSize (order : Int) : Double
```


## <a name="input"></a><span data-ttu-id="b4255-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b4255-106">Input</span></span>

### <a name="order--int"></a><span data-ttu-id="b4255-107">Reihenfolge: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b4255-107">order : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--double"></a><span data-ttu-id="b4255-108">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="b4255-108">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="remarks"></a><span data-ttu-id="b4255-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b4255-109">Remarks</span></span>

<span data-ttu-id="b4255-110">Bei diesem Vorgang wird eine andere Indizierungs Konvention verwendet als [quant-ph/0508139](https://arxiv.org/abs/quant-ph/0508139).</span><span class="sxs-lookup"><span data-stu-id="b4255-110">This operation uses a different indexing convention than that of [quant-ph/0508139](https://arxiv.org/abs/quant-ph/0508139).</span></span> <span data-ttu-id="b4255-111">Dies entspricht insbesondere `DecomposedIntoTimeStepsCA(_, 4)` dem skalaren $p _2 (\lambda) $ in quant-ph/0508139.</span><span class="sxs-lookup"><span data-stu-id="b4255-111">In particular, `DecomposedIntoTimeStepsCA(_, 4)` corresponds to the scalar $p_2(\lambda)$ in quant-ph/0508139.</span></span>
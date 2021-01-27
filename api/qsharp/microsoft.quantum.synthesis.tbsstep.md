---
uid: Microsoft.Quantum.Synthesis.TBSStep
title: Tbsstep-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: TBSStep
qsharp.summary: Computes gate masks to transform perm[x] to x and updates the current permutation.
ms.openlocfilehash: 8980cd359c2159d875444acb727290d1dc9a1b38
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855287"
---
# <a name="tbsstep-function"></a><span data-ttu-id="4a8a2-102">Tbsstep-Funktion</span><span class="sxs-lookup"><span data-stu-id="4a8a2-102">TBSStep function</span></span>

<span data-ttu-id="4a8a2-103">Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="4a8a2-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="4a8a2-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4a8a2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4a8a2-105">Berechnet Gate-Masken zum Transformieren von Perm [x] in x und aktualisiert die aktuelle Permutation.</span><span class="sxs-lookup"><span data-stu-id="4a8a2-105">Computes gate masks to transform perm[x] to x and updates the current permutation.</span></span>

```qsharp
function TBSStep (state : (Int[], Microsoft.Quantum.Synthesis.MCMTMask[]), x : Int) : (Int[], Microsoft.Quantum.Synthesis.MCMTMask[])
```


## <a name="input"></a><span data-ttu-id="4a8a2-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4a8a2-106">Input</span></span>

### <a name="state--intmcmtmask"></a><span data-ttu-id="4a8a2-107">State: ([int](xref:microsoft.quantum.lang-ref.int)[],[mcmtmask](xref:Microsoft.Quantum.Synthesis.MCMTMask)[])</span><span class="sxs-lookup"><span data-stu-id="4a8a2-107">state : ([Int](xref:microsoft.quantum.lang-ref.int)[],[MCMTMask](xref:Microsoft.Quantum.Synthesis.MCMTMask)[])</span></span>




### <a name="x--int"></a><span data-ttu-id="4a8a2-108">x: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4a8a2-108">x : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--intmcmtmask"></a><span data-ttu-id="4a8a2-109">Ausgabe: ([int](xref:microsoft.quantum.lang-ref.int)[],[mcmtmask](xref:Microsoft.Quantum.Synthesis.MCMTMask)[])</span><span class="sxs-lookup"><span data-stu-id="4a8a2-109">Output : ([Int](xref:microsoft.quantum.lang-ref.int)[],[MCMTMask](xref:Microsoft.Quantum.Synthesis.MCMTMask)[])</span></span>


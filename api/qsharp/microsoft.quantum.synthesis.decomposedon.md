---
uid: Microsoft.Quantum.Synthesis.DecomposedOn
title: Debug-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: DecomposedOn
qsharp.summary: Decomposes a permutation on a variable
ms.openlocfilehash: b033723a50fb85e77c9d4baec1f94231327e9b25
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725216"
---
# <a name="decomposedon-function"></a><span data-ttu-id="f511d-102">Debug-Funktion</span><span class="sxs-lookup"><span data-stu-id="f511d-102">DecomposedOn function</span></span>

<span data-ttu-id="f511d-103">Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="f511d-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="f511d-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f511d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f511d-105">Zerlegt eine permutations für eine Variable.</span><span class="sxs-lookup"><span data-stu-id="f511d-105">Decomposes a permutation on a variable</span></span>

```qsharp
function DecomposedOn (perm : Int[], index : Int) : ((Int[], Int[]), Int[])
```


## <a name="description"></a><span data-ttu-id="f511d-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f511d-106">Description</span></span>

<span data-ttu-id="f511d-107">Bei Angabe einer permutations $ \pi $ ( `perm` ) und eines Index $i $ ( `index` ), diese Methode gibt drei Permutationen $ ((\ pi_l, \ pi_r), \pi ') $ so zurück, dass die Bilder von $ \ pi_l $ und $ \ pi_r $ Bits in ihren Elementen bei anderen Indizes als $i $ und Bilder von $ \pi ' $ do not Change Bit $i $ in ihren Elementen nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="f511d-107">Given a permutation $\pi$ (`perm`) and an index $i$ (`index`), this method returns three permutations $((\pi_l, \pi_r), \pi')$ such that the images of $\pi_l$ and $\pi_r$ do not change bits in their elements at indexes other than $i$ and images of $\pi'$ do not change bit $i$ in their elements.</span></span>

## <a name="input"></a><span data-ttu-id="f511d-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f511d-108">Input</span></span>

### <a name="perm--int"></a><span data-ttu-id="f511d-109">Perm: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="f511d-109">perm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>




### <a name="index--int"></a><span data-ttu-id="f511d-110">Index: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f511d-110">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--intintint"></a><span data-ttu-id="f511d-111">Ausgabe: (([int](xref:microsoft.quantum.lang-ref.int)[],[int](xref:microsoft.quantum.lang-ref.int)[]),[int](xref:microsoft.quantum.lang-ref.int)[])</span><span class="sxs-lookup"><span data-stu-id="f511d-111">Output : (([Int](xref:microsoft.quantum.lang-ref.int)[],[Int](xref:microsoft.quantum.lang-ref.int)[]),[Int](xref:microsoft.quantum.lang-ref.int)[])</span></span>


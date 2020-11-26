---
uid: Microsoft.Quantum.Synthesis.DecomposedOn
title: Debug-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: DecomposedOn
qsharp.summary: Decomposes a permutation on a variable
ms.openlocfilehash: 79f952e7bc7ba9f5337cf5e7a625e0d270a2e17a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203228"
---
# <a name="decomposedon-function"></a><span data-ttu-id="ee986-102">Debug-Funktion</span><span class="sxs-lookup"><span data-stu-id="ee986-102">DecomposedOn function</span></span>

<span data-ttu-id="ee986-103">Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="ee986-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="ee986-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ee986-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ee986-105">Zerlegt eine permutations für eine Variable.</span><span class="sxs-lookup"><span data-stu-id="ee986-105">Decomposes a permutation on a variable</span></span>

```qsharp
function DecomposedOn (perm : Int[], index : Int) : ((Int[], Int[]), Int[])
```


## <a name="description"></a><span data-ttu-id="ee986-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ee986-106">Description</span></span>

<span data-ttu-id="ee986-107">Bei Angabe einer permutations $ \pi $ ( `perm` ) und eines Index $i $ ( `index` ), diese Methode gibt drei Permutationen $ ((\ pi_l, \ pi_r), \pi ') $ so zurück, dass die Bilder von $ \ pi_l $ und $ \ pi_r $ Bits in ihren Elementen bei anderen Indizes als $i $ und Bilder von $ \pi ' $ do not Change Bit $i $ in ihren Elementen nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="ee986-107">Given a permutation $\pi$ (`perm`) and an index $i$ (`index`), this method returns three permutations $((\pi_l, \pi_r), \pi')$ such that the images of $\pi_l$ and $\pi_r$ do not change bits in their elements at indexes other than $i$ and images of $\pi'$ do not change bit $i$ in their elements.</span></span>

## <a name="input"></a><span data-ttu-id="ee986-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ee986-108">Input</span></span>

### <a name="perm--int"></a><span data-ttu-id="ee986-109">Perm: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="ee986-109">perm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>




### <a name="index--int"></a><span data-ttu-id="ee986-110">Index: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ee986-110">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--intintint"></a><span data-ttu-id="ee986-111">Ausgabe: (([int](xref:microsoft.quantum.lang-ref.int)[],[int](xref:microsoft.quantum.lang-ref.int)[]),[int](xref:microsoft.quantum.lang-ref.int)[])</span><span class="sxs-lookup"><span data-stu-id="ee986-111">Output : (([Int](xref:microsoft.quantum.lang-ref.int)[],[Int](xref:microsoft.quantum.lang-ref.int)[]),[Int](xref:microsoft.quantum.lang-ref.int)[])</span></span>


---
uid: Microsoft.Quantum.Synthesis.DecompositionState
title: Benutzerdefinierter Typ "decompositionstate"
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: DecompositionState
qsharp.summary: State during decomposition based on variable indexes
ms.openlocfilehash: cd2a55013f1232d4158dd6c33143b7cf6c0aafbc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203194"
---
# <a name="decompositionstate-user-defined-type"></a><span data-ttu-id="6e3e0-102">Benutzerdefinierter Typ "decompositionstate"</span><span class="sxs-lookup"><span data-stu-id="6e3e0-102">DecompositionState user defined type</span></span>

<span data-ttu-id="6e3e0-103">Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="6e3e0-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="6e3e0-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6e3e0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6e3e0-105">Zustand während der Zerlegung basierend auf Variablen Indizes</span><span class="sxs-lookup"><span data-stu-id="6e3e0-105">State during decomposition based on variable indexes</span></span>

```qsharp

newtype DecompositionState = (Perm : Int[], Lfunctions : (BigInt, Int)[], Rfunctions : (BigInt, Int)[]);
```



## <a name="named-items"></a><span data-ttu-id="6e3e0-106">Benannte Elemente</span><span class="sxs-lookup"><span data-stu-id="6e3e0-106">Named Items</span></span>

### <a name="perm--int"></a><span data-ttu-id="6e3e0-107">Perm: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="6e3e0-107">Perm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>


### <a name="lfunctions--bigintint"></a><span data-ttu-id="6e3e0-108">Lfunctions: ([bigint](xref:microsoft.quantum.lang-ref.bigint),[int](xref:microsoft.quantum.lang-ref.int)) []</span><span class="sxs-lookup"><span data-stu-id="6e3e0-108">Lfunctions : ([BigInt](xref:microsoft.quantum.lang-ref.bigint),[Int](xref:microsoft.quantum.lang-ref.int))[]</span></span>


### <a name="rfunctions--bigintint"></a><span data-ttu-id="6e3e0-109">Rfunctions: ([bigint](xref:microsoft.quantum.lang-ref.bigint),[int](xref:microsoft.quantum.lang-ref.int)) []</span><span class="sxs-lookup"><span data-stu-id="6e3e0-109">Rfunctions : ([BigInt](xref:microsoft.quantum.lang-ref.bigint),[Int](xref:microsoft.quantum.lang-ref.int))[]</span></span>



## <a name="description"></a><span data-ttu-id="6e3e0-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6e3e0-110">Description</span></span>

<span data-ttu-id="6e3e0-111">Der-Zustand enthält die aktuelle permutations und die derzeit generierten Funktionen für gesteuerte Gates auf der linken Seite und kontrollierte Gates auf der rechten Seite.</span><span class="sxs-lookup"><span data-stu-id="6e3e0-111">The state holds the current permutation and the currently generated functions for controlled gates on the left, and controlled gates on the right.</span></span>
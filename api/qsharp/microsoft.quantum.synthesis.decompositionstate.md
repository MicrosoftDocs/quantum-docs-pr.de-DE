---
uid: Microsoft.Quantum.Synthesis.DecompositionState
title: Benutzerdefinierter Typ "decompositionstate"
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: DecompositionState
qsharp.summary: State during decomposition based on variable indexes
ms.openlocfilehash: 0547c04828a80b4f696cc17e13c8cc57d0379f96
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725215"
---
# <a name="decompositionstate-user-defined-type"></a><span data-ttu-id="c0c3f-102">Benutzerdefinierter Typ "decompositionstate"</span><span class="sxs-lookup"><span data-stu-id="c0c3f-102">DecompositionState user defined type</span></span>

<span data-ttu-id="c0c3f-103">Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="c0c3f-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="c0c3f-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c0c3f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c0c3f-105">Zustand während der Zerlegung basierend auf Variablen Indizes</span><span class="sxs-lookup"><span data-stu-id="c0c3f-105">State during decomposition based on variable indexes</span></span>

```qsharp

newtype DecompositionState = (Perm : Int[], Lfunctions : (BigInt, Int)[], Rfunctions : (BigInt, Int)[]);
```



## <a name="named-items"></a><span data-ttu-id="c0c3f-106">Benannte Elemente</span><span class="sxs-lookup"><span data-stu-id="c0c3f-106">Named Items</span></span>

### <a name="perm--int"></a><span data-ttu-id="c0c3f-107">Perm: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="c0c3f-107">Perm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>


### <a name="lfunctions--bigintint"></a><span data-ttu-id="c0c3f-108">Lfunctions: ([bigint](xref:microsoft.quantum.lang-ref.bigint),[int](xref:microsoft.quantum.lang-ref.int)) []</span><span class="sxs-lookup"><span data-stu-id="c0c3f-108">Lfunctions : ([BigInt](xref:microsoft.quantum.lang-ref.bigint),[Int](xref:microsoft.quantum.lang-ref.int))[]</span></span>


### <a name="rfunctions--bigintint"></a><span data-ttu-id="c0c3f-109">Rfunctions: ([bigint](xref:microsoft.quantum.lang-ref.bigint),[int](xref:microsoft.quantum.lang-ref.int)) []</span><span class="sxs-lookup"><span data-stu-id="c0c3f-109">Rfunctions : ([BigInt](xref:microsoft.quantum.lang-ref.bigint),[Int](xref:microsoft.quantum.lang-ref.int))[]</span></span>



## <a name="description"></a><span data-ttu-id="c0c3f-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c0c3f-110">Description</span></span>

<span data-ttu-id="c0c3f-111">Der-Zustand enthält die aktuelle permutations und die derzeit generierten Funktionen für gesteuerte Gates auf der linken Seite und kontrollierte Gates auf der rechten Seite.</span><span class="sxs-lookup"><span data-stu-id="c0c3f-111">The state holds the current permutation and the currently generated functions for controlled gates on the left, and controlled gates on the right.</span></span>
---
uid: Microsoft.Quantum.Synthesis.TruthTablesFromPermutationFolder
title: Trutablesfrompermutationfolder-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: TruthTablesFromPermutationFolder
qsharp.summary: Decomposition logic for a single variable index
ms.openlocfilehash: 86e112782825303805029b2f9f6cfd9d6ce9e8b6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96231023"
---
# <a name="truthtablesfrompermutationfolder-function"></a><span data-ttu-id="6b89b-102">Trutablesfrompermutationfolder-Funktion</span><span class="sxs-lookup"><span data-stu-id="6b89b-102">TruthTablesFromPermutationFolder function</span></span>

<span data-ttu-id="6b89b-103">Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="6b89b-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="6b89b-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6b89b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6b89b-105">Zerlegungs Logik für einen einzelnen Variablen Index</span><span class="sxs-lookup"><span data-stu-id="6b89b-105">Decomposition logic for a single variable index</span></span>

```qsharp
function TruthTablesFromPermutationFolder (numVars : Int, state : Microsoft.Quantum.Synthesis.DecompositionState, index : Int) : Microsoft.Quantum.Synthesis.DecompositionState
```


## <a name="description"></a><span data-ttu-id="6b89b-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6b89b-106">Description</span></span>

<span data-ttu-id="6b89b-107">Dies nimmt den aktuellen Zustand an und generiert eine aktualisierte permutations und fügt ggf. neue Funktionen für kontrollierte Gates hinzu.</span><span class="sxs-lookup"><span data-stu-id="6b89b-107">This takes the current state and generates an updated permutation and possibly adds new functions for controlled gates.</span></span>

## <a name="input"></a><span data-ttu-id="6b89b-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6b89b-108">Input</span></span>

### <a name="numvars--int"></a><span data-ttu-id="6b89b-109">numvars: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6b89b-109">numVars : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="state--decompositionstate"></a><span data-ttu-id="6b89b-110">Status: " [außerpositionzustand](xref:Microsoft.Quantum.Synthesis.DecompositionState) "</span><span class="sxs-lookup"><span data-stu-id="6b89b-110">state : [DecompositionState](xref:Microsoft.Quantum.Synthesis.DecompositionState)</span></span>




### <a name="index--int"></a><span data-ttu-id="6b89b-111">Index: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6b89b-111">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--decompositionstate"></a><span data-ttu-id="6b89b-112">Ausgabe: [decompositionstate](xref:Microsoft.Quantum.Synthesis.DecompositionState)</span><span class="sxs-lookup"><span data-stu-id="6b89b-112">Output : [DecompositionState](xref:Microsoft.Quantum.Synthesis.DecompositionState)</span></span>


---
uid: Microsoft.Quantum.Synthesis.TruthTablesFromPermutationFolder
title: Trutablesfrompermutationfolder-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: TruthTablesFromPermutationFolder
qsharp.summary: Decomposition logic for a single variable index
ms.openlocfilehash: 6b00c9e880ed7b7b3bf446dcb17dab3bab7a83a7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724459"
---
# <a name="truthtablesfrompermutationfolder-function"></a><span data-ttu-id="838c4-102">Trutablesfrompermutationfolder-Funktion</span><span class="sxs-lookup"><span data-stu-id="838c4-102">TruthTablesFromPermutationFolder function</span></span>

<span data-ttu-id="838c4-103">Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="838c4-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="838c4-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="838c4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="838c4-105">Zerlegungs Logik für einen einzelnen Variablen Index</span><span class="sxs-lookup"><span data-stu-id="838c4-105">Decomposition logic for a single variable index</span></span>

```qsharp
function TruthTablesFromPermutationFolder (numVars : Int, state : Microsoft.Quantum.Synthesis.DecompositionState, index : Int) : Microsoft.Quantum.Synthesis.DecompositionState
```


## <a name="description"></a><span data-ttu-id="838c4-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="838c4-106">Description</span></span>

<span data-ttu-id="838c4-107">Dies nimmt den aktuellen Zustand an und generiert eine aktualisierte permutations und fügt ggf. neue Funktionen für kontrollierte Gates hinzu.</span><span class="sxs-lookup"><span data-stu-id="838c4-107">This takes the current state and generates an updated permutation and possibly adds new functions for controlled gates.</span></span>

## <a name="input"></a><span data-ttu-id="838c4-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="838c4-108">Input</span></span>

### <a name="numvars--int"></a><span data-ttu-id="838c4-109">numvars: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="838c4-109">numVars : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="state--decompositionstate"></a><span data-ttu-id="838c4-110">Status: " [außerpositionzustand](xref:Microsoft.Quantum.Synthesis.DecompositionState) "</span><span class="sxs-lookup"><span data-stu-id="838c4-110">state : [DecompositionState](xref:Microsoft.Quantum.Synthesis.DecompositionState)</span></span>




### <a name="index--int"></a><span data-ttu-id="838c4-111">Index: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="838c4-111">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--decompositionstate"></a><span data-ttu-id="838c4-112">Ausgabe: [decompositionstate](xref:Microsoft.Quantum.Synthesis.DecompositionState)</span><span class="sxs-lookup"><span data-stu-id="838c4-112">Output : [DecompositionState](xref:Microsoft.Quantum.Synthesis.DecompositionState)</span></span>


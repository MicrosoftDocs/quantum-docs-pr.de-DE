---
uid: Microsoft.Quantum.Synthesis.TruthTablesFromPermutationFolder
title: Trutablesfrompermutationfolder-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: TruthTablesFromPermutationFolder
qsharp.summary: Decomposition logic for a single variable index
ms.openlocfilehash: 881bb8e29d3d7761cc521837502ea79b0714b381
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855251"
---
# <a name="truthtablesfrompermutationfolder-function"></a><span data-ttu-id="8848c-102">Trutablesfrompermutationfolder-Funktion</span><span class="sxs-lookup"><span data-stu-id="8848c-102">TruthTablesFromPermutationFolder function</span></span>

<span data-ttu-id="8848c-103">Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="8848c-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="8848c-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8848c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8848c-105">Zerlegungs Logik für einen einzelnen Variablen Index</span><span class="sxs-lookup"><span data-stu-id="8848c-105">Decomposition logic for a single variable index</span></span>

```qsharp
function TruthTablesFromPermutationFolder (numVars : Int, state : Microsoft.Quantum.Synthesis.DecompositionState, index : Int) : Microsoft.Quantum.Synthesis.DecompositionState
```


## <a name="description"></a><span data-ttu-id="8848c-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8848c-106">Description</span></span>

<span data-ttu-id="8848c-107">Dies nimmt den aktuellen Zustand an und generiert eine aktualisierte permutations und fügt ggf. neue Funktionen für kontrollierte Gates hinzu.</span><span class="sxs-lookup"><span data-stu-id="8848c-107">This takes the current state and generates an updated permutation and possibly adds new functions for controlled gates.</span></span>

## <a name="input"></a><span data-ttu-id="8848c-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8848c-108">Input</span></span>

### <a name="numvars--int"></a><span data-ttu-id="8848c-109">numvars: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8848c-109">numVars : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="state--decompositionstate"></a><span data-ttu-id="8848c-110">Status: " [außerpositionzustand](xref:Microsoft.Quantum.Synthesis.DecompositionState) "</span><span class="sxs-lookup"><span data-stu-id="8848c-110">state : [DecompositionState](xref:Microsoft.Quantum.Synthesis.DecompositionState)</span></span>




### <a name="index--int"></a><span data-ttu-id="8848c-111">Index: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8848c-111">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--decompositionstate"></a><span data-ttu-id="8848c-112">Ausgabe: [decompositionstate](xref:Microsoft.Quantum.Synthesis.DecompositionState)</span><span class="sxs-lookup"><span data-stu-id="8848c-112">Output : [DecompositionState](xref:Microsoft.Quantum.Synthesis.DecompositionState)</span></span>


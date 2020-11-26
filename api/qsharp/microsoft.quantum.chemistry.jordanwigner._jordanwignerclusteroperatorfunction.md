---
uid: Microsoft.Quantum.Chemistry.JordanWigner._JordanWignerClusterOperatorFunction
title: _JordanWignerClusterOperatorFunction-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _JordanWignerClusterOperatorFunction
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the JordanWigner basis.
ms.openlocfilehash: 023ac4a6aaee8e3d0514a471c33c575b86004b15
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203822"
---
# <a name="_jordanwignerclusteroperatorfunction-function"></a><span data-ttu-id="04ab4-102">_JordanWignerClusterOperatorFunction-Funktion</span><span class="sxs-lookup"><span data-stu-id="04ab4-102">_JordanWignerClusterOperatorFunction function</span></span>

<span data-ttu-id="04ab4-103">Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="04ab4-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="04ab4-104">Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="04ab4-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="04ab4-105">Stellt einen dynamischen Generator als Satz von simulier baren Gates und eine Erweiterung in der jordanwigner-Basis dar.</span><span class="sxs-lookup"><span data-stu-id="04ab4-105">Represents a dynamical generator as a set of simulatable gates and an expansion in the JordanWigner basis.</span></span>

```qsharp
function _JordanWignerClusterOperatorFunction (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Simulation.EvolutionUnitary
```


## <a name="input"></a><span data-ttu-id="04ab4-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="04ab4-106">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="04ab4-107">generatorindex: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="04ab4-107">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="04ab4-108">Ein Generator Index, der als einheitliche Evolution in der jordanwigner dargestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="04ab4-108">A generator index to be represented as unitary evolution in the JordanWigner.</span></span>



## <a name="output--evolutionunitary"></a><span data-ttu-id="04ab4-109">Ausgabe: [evolutioneinheitlich](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)</span><span class="sxs-lookup"><span data-stu-id="04ab4-109">Output : [EvolutionUnitary](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)</span></span>

<span data-ttu-id="04ab4-110">Ein, `EvolutionUnitary` der die Zeitentwicklung durch den in ' generatorindex ' referenzierten Begriff darstellt.</span><span class="sxs-lookup"><span data-stu-id="04ab4-110">An `EvolutionUnitary` representing time-evolution by the term referenced in \`generatorIndex.</span></span>
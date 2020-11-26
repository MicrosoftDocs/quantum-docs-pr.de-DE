---
uid: Microsoft.Quantum.Simulation.GeneratorIndex
title: Benutzerdefinierter generatorindex-Typ
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: GeneratorIndex
qsharp.summary: >-
  Represents a single primitive term in the set of all dynamical generators, e.g. Hermitian operators, for which there exists a map from that generator to time-evolution by that generator, through `EvolutionSet`.

  The first element (Int[], Double[]) is indexes that single term -- For instance, the Pauli string XXY with coefficient 0.5 would be indexed by ([1,1,2], [0.5]). Alternatively, Hamiltonians parameterized by a continuous variable, such as X cos φ + Y sin φ, might for instance be represented by ([], [φ]). The second element indexes the subsystem on which the generator acts on.
ms.openlocfilehash: dae23db9bee34be4aa99d96799efad64a66d7193
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229323"
---
# <a name="generatorindex-user-defined-type"></a><span data-ttu-id="05c84-102">Benutzerdefinierter generatorindex-Typ</span><span class="sxs-lookup"><span data-stu-id="05c84-102">GeneratorIndex user defined type</span></span>

<span data-ttu-id="05c84-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="05c84-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="05c84-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="05c84-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="05c84-105">Stellt einen einzelnen primitiven Begriff in der Menge aller dynamischen Generatoren dar, z. b. "hermitian"-Operatoren, für die eine Zuordnung von diesem Generator zur Zeit Weiterentwicklung durch diesen Generator vorhanden ist `EvolutionSet` .</span><span class="sxs-lookup"><span data-stu-id="05c84-105">Represents a single primitive term in the set of all dynamical generators, e.g. Hermitian operators, for which there exists a map from that generator to time-evolution by that generator, through `EvolutionSet`.</span></span>

<span data-ttu-id="05c84-106">Beim ersten Element (int [], Double []) handelt es sich um Indizes, die einen einzelnen Begriff aufweisen. beispielsweise wird die Pauli-Zeichenfolge XXY mit Koeffizient 0,5 von ([1, 1, 2], [0,5]) indiziert.</span><span class="sxs-lookup"><span data-stu-id="05c84-106">The first element (Int[], Double[]) is indexes that single term -- For instance, the Pauli string XXY with coefficient 0.5 would be indexed by ([1,1,2], [0.5]).</span></span> <span data-ttu-id="05c84-107">Alternativ kann hamiltonane, die durch eine kontinuierliche Variable, wie z. b. X cos und Y Sin, parametrisiert werden, z. b. durch ([], [ge]) dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="05c84-107">Alternatively, Hamiltonians parameterized by a continuous variable, such as X cos φ + Y sin φ, might for instance be represented by ([], [φ]).</span></span> <span data-ttu-id="05c84-108">Das zweite Element indiziert das Subsystem, auf dem der Generator agiert.</span><span class="sxs-lookup"><span data-stu-id="05c84-108">The second element indexes the subsystem on which the generator acts on.</span></span>

```qsharp

newtype GeneratorIndex = ((Int[], Double[]), Int[]);
```



## <a name="remarks"></a><span data-ttu-id="05c84-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="05c84-109">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="05c84-110">Die Interpretation eines `GeneratorIndex` ist nicht definiert, außer mit einem Verweis auf einen bestimmten Satz von Generatoren.</span><span class="sxs-lookup"><span data-stu-id="05c84-110">The interpretation of an `GeneratorIndex` is not defined except with reference to a particular set of generators.</span></span>

## <a name="see-also"></a><span data-ttu-id="05c84-111">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="05c84-111">See Also</span></span>

- [<span data-ttu-id="05c84-112">Microsoft. Quantum. Simulation. evolutionset</span><span class="sxs-lookup"><span data-stu-id="05c84-112">Microsoft.Quantum.Simulation.EvolutionSet</span></span>](xref:Microsoft.Quantum.Simulation.EvolutionSet)
- [<span data-ttu-id="05c84-113">Microsoft. Quantum. Simulation. paulievolutionset</span><span class="sxs-lookup"><span data-stu-id="05c84-113">Microsoft.Quantum.Simulation.PauliEvolutionSet</span></span>](xref:Microsoft.Quantum.Simulation.PauliEvolutionSet)
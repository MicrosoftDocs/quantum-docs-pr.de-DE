---
uid: Microsoft.Quantum.Simulation.PauliEvolutionFunction
title: Paulievolutionfunction-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliEvolutionFunction
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.
ms.openlocfilehash: 9b12dc4a05c99aad319799f8c6526cd3085e6dcd
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847980"
---
# <a name="paulievolutionfunction-function"></a><span data-ttu-id="a91d6-102">Paulievolutionfunction-Funktion</span><span class="sxs-lookup"><span data-stu-id="a91d6-102">PauliEvolutionFunction function</span></span>

<span data-ttu-id="a91d6-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="a91d6-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="a91d6-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a91d6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a91d6-105">Stellt einen dynamischen Generator als Satz von simulsierbaren Gates und eine Erweiterung in der Pauli-Basis dar.</span><span class="sxs-lookup"><span data-stu-id="a91d6-105">Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.</span></span>

```qsharp
function PauliEvolutionFunction (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Simulation.EvolutionUnitary
```


## <a name="input"></a><span data-ttu-id="a91d6-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a91d6-106">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="a91d6-107">generatorindex: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="a91d6-107">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="a91d6-108">Ein Generator Index, der im Pauli als einheitliche Evolution dargestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a91d6-108">A generator index to be represented as unitary evolution in the Pauli basis.</span></span>



## <a name="output--evolutionunitary"></a><span data-ttu-id="a91d6-109">Ausgabe: [evolutioneinheitlich](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)</span><span class="sxs-lookup"><span data-stu-id="a91d6-109">Output : [EvolutionUnitary](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)</span></span>

<span data-ttu-id="a91d6-110">Ein, `EvolutionUnitary` der die Zeitentwicklung durch den in ' generatorindex ' referenzierten Begriff darstellt.</span><span class="sxs-lookup"><span data-stu-id="a91d6-110">An `EvolutionUnitary` representing time-evolution by the term referenced in \`generatorIndex.</span></span>
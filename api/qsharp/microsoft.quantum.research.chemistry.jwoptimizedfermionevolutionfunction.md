---
uid: Microsoft.Quantum.Research.Chemistry.JWOptimizedFermionEvolutionFunction
title: Jwoptimizedfermionevolutionfunction-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: JWOptimizedFermionEvolutionFunction
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the JWOptimized basis.
ms.openlocfilehash: 952f3dc4ab0595ace0ee34c040cb21969afa111f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701825"
---
# <a name="jwoptimizedfermionevolutionfunction-function"></a><span data-ttu-id="47e14-102">Jwoptimizedfermionevolutionfunction-Funktion</span><span class="sxs-lookup"><span data-stu-id="47e14-102">JWOptimizedFermionEvolutionFunction function</span></span>

<span data-ttu-id="47e14-103">Namespace: [Microsoft. Quantum. Research. Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="47e14-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="47e14-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="47e14-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="47e14-105">Stellt einen dynamischen Generator als eine Reihe von simulier baren Gates und eine Erweiterung in der jwoptimierte-Basis dar.</span><span class="sxs-lookup"><span data-stu-id="47e14-105">Represents a dynamical generator as a set of simulatable gates and an expansion in the JWOptimized basis.</span></span>

```qsharp
function JWOptimizedFermionEvolutionFunction (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex, parityQubit : Qubit) : Microsoft.Quantum.Simulation.EvolutionUnitary
```


## <a name="input"></a><span data-ttu-id="47e14-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="47e14-106">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="47e14-107">generatorindex: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="47e14-107">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="47e14-108">Ein Generator Index, der in der jwoptimierte-Basis als einheitliche Evolution dargestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="47e14-108">A generator index to be represented as unitary evolution in the JWOptimized basis.</span></span>


### <a name="parityqubit--qubit"></a><span data-ttu-id="47e14-109">parameteryqubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="47e14-109">parityQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="47e14-110">Qubit, das das Vorzeichen der Zeitentwicklung bestimmt.</span><span class="sxs-lookup"><span data-stu-id="47e14-110">Qubit that determines the sign of time-evolution.</span></span>



## <a name="output--evolutionunitary"></a><span data-ttu-id="47e14-111">Ausgabe: [evolutioneinheitlich](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)</span><span class="sxs-lookup"><span data-stu-id="47e14-111">Output : [EvolutionUnitary](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)</span></span>

<span data-ttu-id="47e14-112">Ein, `EvolutionUnitary` der die Zeitentwicklung durch den in ' generatorindex ' referenzierten Begriff darstellt.</span><span class="sxs-lookup"><span data-stu-id="47e14-112">An `EvolutionUnitary` representing time-evolution by the term referenced in \`generatorIndex.</span></span>
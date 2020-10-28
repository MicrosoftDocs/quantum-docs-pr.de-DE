---
uid: Microsoft.Quantum.Simulation.PauliEvolutionFunction
title: Paulievolutionfunction-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliEvolutionFunction
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.
ms.openlocfilehash: 060f4e4f23bb8b47518a3a22bbca8ab0be6e13b7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706663"
---
# <a name="paulievolutionfunction-function"></a><span data-ttu-id="9153c-102">Paulievolutionfunction-Funktion</span><span class="sxs-lookup"><span data-stu-id="9153c-102">PauliEvolutionFunction function</span></span>

<span data-ttu-id="9153c-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="9153c-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="9153c-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9153c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9153c-105">Stellt einen dynamischen Generator als Satz von simulsierbaren Gates und eine Erweiterung in der Pauli-Basis dar.</span><span class="sxs-lookup"><span data-stu-id="9153c-105">Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.</span></span>

```qsharp
function PauliEvolutionFunction (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Simulation.EvolutionUnitary
```


## <a name="input"></a><span data-ttu-id="9153c-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9153c-106">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="9153c-107">generatorindex: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="9153c-107">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="9153c-108">Ein Generator Index, der im Pauli als einheitliche Evolution dargestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9153c-108">A generator index to be represented as unitary evolution in the Pauli basis.</span></span>



## <a name="output--evolutionunitary"></a><span data-ttu-id="9153c-109">Ausgabe: [evolutioneinheitlich](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)</span><span class="sxs-lookup"><span data-stu-id="9153c-109">Output : [EvolutionUnitary](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)</span></span>

<span data-ttu-id="9153c-110">Ein, `EvolutionUnitary` der die Zeitentwicklung durch den in ' generatorindex ' referenzierten Begriff darstellt.</span><span class="sxs-lookup"><span data-stu-id="9153c-110">An `EvolutionUnitary` representing time-evolution by the term referenced in \`generatorIndex.</span></span>
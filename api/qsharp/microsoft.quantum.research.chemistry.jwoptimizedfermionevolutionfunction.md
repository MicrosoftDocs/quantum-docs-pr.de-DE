---
uid: Microsoft.Quantum.Research.Chemistry.JWOptimizedFermionEvolutionFunction
title: Jwoptimizedfermionevolutionfunction-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: JWOptimizedFermionEvolutionFunction
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the JWOptimized basis.
ms.openlocfilehash: d70bea8fcb5bd82ddad6dcd2b67c3eb178283bb3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857868"
---
# <a name="jwoptimizedfermionevolutionfunction-function"></a>Jwoptimizedfermionevolutionfunction-Funktion

Namespace: [Microsoft. Quantum. Research. Chemistry](xref:Microsoft.Quantum.Research.Chemistry)

Paket: [Microsoft. Quantum. Research. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)


Stellt einen dynamischen Generator als eine Reihe von simulier baren Gates und eine Erweiterung in der jwoptimierte-Basis dar.

```qsharp
function JWOptimizedFermionEvolutionFunction (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex, parityQubit : Qubit) : Microsoft.Quantum.Simulation.EvolutionUnitary
```


## <a name="input"></a>Eingabe

### <a name="generatorindex--generatorindex"></a>generatorindex: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

Ein Generator Index, der in der jwoptimierte-Basis als einheitliche Evolution dargestellt werden soll.


### <a name="parityqubit--qubit"></a>parameteryqubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Qubit, das das Vorzeichen der Zeitentwicklung bestimmt.



## <a name="output--evolutionunitary"></a>Ausgabe: [evolutioneinheitlich](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)

Ein, `EvolutionUnitary` der die Zeitentwicklung durch den in ' generatorindex ' referenzierten Begriff darstellt.
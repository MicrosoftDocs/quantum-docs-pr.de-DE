---
uid: Microsoft.Quantum.Research.Chemistry.JordanWignerOptimizedFermionEvolutionSet
title: Jordanwigneroptimizedfermionevolutionset-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: JordanWignerOptimizedFermionEvolutionSet
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.
ms.openlocfilehash: 2cd555882792c29cb2ed71972739505df11fbabc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225736"
---
# <a name="jordanwigneroptimizedfermionevolutionset-function"></a>Jordanwigneroptimizedfermionevolutionset-Funktion

Namespace: [Microsoft. Quantum. Research. Chemistry](xref:Microsoft.Quantum.Research.Chemistry)

Paket: [Microsoft. Quantum. Research. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)


Stellt einen dynamischen Generator als Satz von simulsierbaren Gates und eine Erweiterung in der Pauli-Basis dar.

```qsharp
function JordanWignerOptimizedFermionEvolutionSet (parityQubit : Qubit) : Microsoft.Quantum.Simulation.EvolutionSet
```


## <a name="input"></a>Eingabe

### <a name="parityqubit--qubit"></a>parameteryqubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Qubit, das das Vorzeichen der Zeitentwicklung bestimmt.



## <a name="output--evolutionset"></a>Ausgabe: [evolutionsatz](xref:Microsoft.Quantum.Simulation.EvolutionSet)

Ein `EvolutionSet` , der einen `GeneratorIndex` für die jwoptimierte-Basis einem ' evolutioneinheitlich ' zuordnet.
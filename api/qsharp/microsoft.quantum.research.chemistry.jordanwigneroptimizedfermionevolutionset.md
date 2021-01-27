---
uid: Microsoft.Quantum.Research.Chemistry.JordanWignerOptimizedFermionEvolutionSet
title: Jordanwigneroptimizedfermionevolutionset-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: JordanWignerOptimizedFermionEvolutionSet
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.
ms.openlocfilehash: 941d66a936ef1a2ac76230d14ca8437ac2a4a049
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857882"
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
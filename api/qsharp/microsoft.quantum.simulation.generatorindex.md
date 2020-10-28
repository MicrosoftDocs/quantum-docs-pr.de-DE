---
uid: Microsoft.Quantum.Simulation.GeneratorIndex
title: Benutzerdefinierter generatorindex-Typ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: GeneratorIndex
qsharp.summary: >-
  Represents a single primitive term in the set of all dynamical generators, e.g. Hermitian operators, for which there exists a map from that generator to time-evolution by that generator, through `EvolutionSet`.

  The first element (Int[], Double[]) is indexes that single term -- For instance, the Pauli string XXY with coefficient 0.5 would be indexed by ([1,1,2], [0.5]). Alternatively, Hamiltonians parameterized by a continuous variable, such as X cos φ + Y sin φ, might for instance be represented by ([], [φ]). The second element indexes the subsystem on which the generator acts on.
ms.openlocfilehash: 8d36f74fbf122469e9e829b950e4ed9a6e3a35a7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723900"
---
# <a name="generatorindex-user-defined-type"></a>Benutzerdefinierter generatorindex-Typ

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paketen [](https://nuget.org/packages/)


Stellt einen einzelnen primitiven Begriff in der Menge aller dynamischen Generatoren dar, z. b. "hermitian"-Operatoren, für die eine Zuordnung von diesem Generator zur Zeit Weiterentwicklung durch diesen Generator vorhanden ist `EvolutionSet` .

Beim ersten Element (int [], Double []) handelt es sich um Indizes, die einen einzelnen Begriff aufweisen. beispielsweise wird die Pauli-Zeichenfolge XXY mit Koeffizient 0,5 von ([1, 1, 2], [0,5]) indiziert. Alternativ kann hamiltonane, die durch eine kontinuierliche Variable, wie z. b. X cos und Y Sin, parametrisiert werden, z. b. durch ([], [ge]) dargestellt werden. Das zweite Element indiziert das Subsystem, auf dem der Generator agiert.

```qsharp

newtype GeneratorIndex = ((Int[], Double[]), Int[]);
```



## <a name="remarks"></a>Hinweise

> [!WARNING]
> Die Interpretation eines `GeneratorIndex` ist nicht definiert, außer mit einem Verweis auf einen bestimmten Satz von Generatoren.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Simulation. evolutionset](xref:Microsoft.Quantum.Simulation.EvolutionSet)
- [Microsoft. Quantum. Simulation. paulievolutionset](xref:Microsoft.Quantum.Simulation.PauliEvolutionSet)
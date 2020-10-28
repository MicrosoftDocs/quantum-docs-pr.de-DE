---
uid: Microsoft.Quantum.Simulation.PauliEvolutionSet
title: Paulievolutionset-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliEvolutionSet
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.
ms.openlocfilehash: 89c81aca4cfad6087d764ac8f5a0f1426e905e4b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722051"
---
# <a name="paulievolutionset-function"></a>Paulievolutionset-Funktion

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paketen [](https://nuget.org/packages/)


Stellt einen dynamischen Generator als Satz von simulsierbaren Gates und eine Erweiterung in der Pauli-Basis dar.

```qsharp
function PauliEvolutionSet () : Microsoft.Quantum.Simulation.EvolutionSet
```


## <a name="output--evolutionset"></a>Ausgabe: [evolutionsatz](xref:Microsoft.Quantum.Simulation.EvolutionSet)

Ein `EvolutionSet` , das eine `GeneratorIndex` für die Pauli-Basis einem ' evolutioneinheitlich ' zuordnet.

## <a name="remarks"></a>Hinweise

Dies wird durch eine partielle Anwendung von erreicht <xref:microsoft.quantum.simulation.paulievolutionfunction> .
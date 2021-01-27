---
uid: Microsoft.Quantum.Simulation.PauliEvolutionSet
title: Paulievolutionset-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliEvolutionSet
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.
ms.openlocfilehash: 961c95e6787b69e35ca531fa36164cc988ad660d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847962"
---
# <a name="paulievolutionset-function"></a>Paulievolutionset-Funktion

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Stellt einen dynamischen Generator als Satz von simulsierbaren Gates und eine Erweiterung in der Pauli-Basis dar.

```qsharp
function PauliEvolutionSet () : Microsoft.Quantum.Simulation.EvolutionSet
```


## <a name="output--evolutionset"></a>Ausgabe: [evolutionsatz](xref:Microsoft.Quantum.Simulation.EvolutionSet)

Ein `EvolutionSet` , das eine `GeneratorIndex` für die Pauli-Basis einem ' evolutioneinheitlich ' zuordnet.

## <a name="remarks"></a>Bemerkungen

Dies wird durch eine partielle Anwendung von erreicht <xref:microsoft.quantum.simulation.paulievolutionfunction> .
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
# <a name="paulievolutionset-function"></a><span data-ttu-id="1d50c-102">Paulievolutionset-Funktion</span><span class="sxs-lookup"><span data-stu-id="1d50c-102">PauliEvolutionSet function</span></span>

<span data-ttu-id="1d50c-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="1d50c-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="1d50c-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1d50c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1d50c-105">Stellt einen dynamischen Generator als Satz von simulsierbaren Gates und eine Erweiterung in der Pauli-Basis dar.</span><span class="sxs-lookup"><span data-stu-id="1d50c-105">Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.</span></span>

```qsharp
function PauliEvolutionSet () : Microsoft.Quantum.Simulation.EvolutionSet
```


## <a name="output--evolutionset"></a><span data-ttu-id="1d50c-106">Ausgabe: [evolutionsatz](xref:Microsoft.Quantum.Simulation.EvolutionSet)</span><span class="sxs-lookup"><span data-stu-id="1d50c-106">Output : [EvolutionSet](xref:Microsoft.Quantum.Simulation.EvolutionSet)</span></span>

<span data-ttu-id="1d50c-107">Ein `EvolutionSet` , das eine `GeneratorIndex` für die Pauli-Basis einem ' evolutioneinheitlich ' zuordnet.</span><span class="sxs-lookup"><span data-stu-id="1d50c-107">An `EvolutionSet` that maps a `GeneratorIndex` for the Pauli basis to an \`EvolutionUnitary.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d50c-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1d50c-108">Remarks</span></span>

<span data-ttu-id="1d50c-109">Dies wird durch eine partielle Anwendung von erreicht <xref:microsoft.quantum.simulation.paulievolutionfunction> .</span><span class="sxs-lookup"><span data-stu-id="1d50c-109">This is obtained by partial application of <xref:microsoft.quantum.simulation.paulievolutionfunction>.</span></span>
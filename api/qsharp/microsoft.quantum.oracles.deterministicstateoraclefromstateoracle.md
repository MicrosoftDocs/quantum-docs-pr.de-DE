---
uid: Microsoft.Quantum.Oracles.DeterministicStateOracleFromStateOracle
title: Deterministicstateoraclefromstateoracle-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: DeterministicStateOracleFromStateOracle
qsharp.summary: Converts an oracle of type `StateOracle` to `DeterministicStateOracle`.
ms.openlocfilehash: af545a7d6e82e654ee36ab3ba77c8f8be3384b96
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854555"
---
# <a name="deterministicstateoraclefromstateoracle-function"></a><span data-ttu-id="5cd60-102">Deterministicstateoraclefromstateoracle-Funktion</span><span class="sxs-lookup"><span data-stu-id="5cd60-102">DeterministicStateOracleFromStateOracle function</span></span>

<span data-ttu-id="5cd60-103">Namespace: [Microsoft. Quantum. Oracles](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="5cd60-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="5cd60-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5cd60-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5cd60-105">Konvertiert ein Oracle vom Typ `StateOracle` in `DeterministicStateOracle` .</span><span class="sxs-lookup"><span data-stu-id="5cd60-105">Converts an oracle of type `StateOracle` to `DeterministicStateOracle`.</span></span>

```qsharp
function DeterministicStateOracleFromStateOracle (idxFlagQubit : Int, stateOracle : Microsoft.Quantum.Oracles.StateOracle) : Microsoft.Quantum.Oracles.DeterministicStateOracle
```


## <a name="input"></a><span data-ttu-id="5cd60-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5cd60-106">Input</span></span>

### <a name="idxflagqubit--int"></a><span data-ttu-id="5cd60-107">idxflagqubit: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5cd60-107">idxFlagQubit : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5cd60-108">Der Index für das Flag-Qubit des `stateOracle` $A $, das explizit für zwei Register agiert: das Flag $f $ und das System $s $, z. b. $A \ket {0} \_ f\ket {\ PSI} \_ s $.</span><span class="sxs-lookup"><span data-stu-id="5cd60-108">The index to the flag qubit of the `stateOracle` $A$, which explicitly acts on two registers: the flag $f$ and the system $s$, e.g. $A\ket{0}\_f\ket{\psi}\_s$.</span></span>


### <a name="stateoracle--stateoracle"></a><span data-ttu-id="5cd60-109">stateoracle: [stateoracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span><span class="sxs-lookup"><span data-stu-id="5cd60-109">stateOracle : [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span></span>

<span data-ttu-id="5cd60-110">Ein Status Vorbereitungs-Oracle $A $ vom Typ `StateOracle` .</span><span class="sxs-lookup"><span data-stu-id="5cd60-110">A state preparation oracle $A$ of type `StateOracle`.</span></span>



## <a name="output--deterministicstateoracle"></a><span data-ttu-id="5cd60-111">Ausgabe: [deterministicstateoracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span><span class="sxs-lookup"><span data-stu-id="5cd60-111">Output : [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span></span>

<span data-ttu-id="5cd60-112">Die gleiche Zustands Vorbereitung ist Oracle $A $, aber jetzt vom Typ `DeterministicStateOracle` , sodass Sie auf ein Register angewendet wird, bei dem $a, s $ nicht mehr explizit getrennt werden, z. b.  $A \ket{0\psi} \_ {As} $.</span><span class="sxs-lookup"><span data-stu-id="5cd60-112">The same state preparation oracle $A$, but now of type `DeterministicStateOracle`, so it acts on a register where $a,s$ no longer explicitly separate, e.g.  $A\ket{0\psi}\_{as}$.</span></span>

## <a name="see-also"></a><span data-ttu-id="5cd60-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5cd60-113">See Also</span></span>

- [<span data-ttu-id="5cd60-114">Microsoft. Quantum. Oracles. stateoracle</span><span class="sxs-lookup"><span data-stu-id="5cd60-114">Microsoft.Quantum.Oracles.StateOracle</span></span>](xref:Microsoft.Quantum.Oracles.StateOracle)
- [<span data-ttu-id="5cd60-115">Microsoft. Quantum. Oracles. deterministicstateoracle</span><span class="sxs-lookup"><span data-stu-id="5cd60-115">Microsoft.Quantum.Oracles.DeterministicStateOracle</span></span>](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)
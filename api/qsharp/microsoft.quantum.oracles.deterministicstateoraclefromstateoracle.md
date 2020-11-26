---
uid: Microsoft.Quantum.Oracles.DeterministicStateOracleFromStateOracle
title: Deterministicstateoraclefromstateoracle-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: DeterministicStateOracleFromStateOracle
qsharp.summary: Converts an oracle of type `StateOracle` to `DeterministicStateOracle`.
ms.openlocfilehash: 183b1108ead6239e26bb0b38144cb9374e7bf285
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226756"
---
# <a name="deterministicstateoraclefromstateoracle-function"></a><span data-ttu-id="48f51-102">Deterministicstateoraclefromstateoracle-Funktion</span><span class="sxs-lookup"><span data-stu-id="48f51-102">DeterministicStateOracleFromStateOracle function</span></span>

<span data-ttu-id="48f51-103">Namespace: [Microsoft. Quantum. Oracles](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="48f51-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="48f51-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="48f51-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="48f51-105">Konvertiert ein Oracle vom Typ `StateOracle` in `DeterministicStateOracle` .</span><span class="sxs-lookup"><span data-stu-id="48f51-105">Converts an oracle of type `StateOracle` to `DeterministicStateOracle`.</span></span>

```qsharp
function DeterministicStateOracleFromStateOracle (idxFlagQubit : Int, stateOracle : Microsoft.Quantum.Oracles.StateOracle) : Microsoft.Quantum.Oracles.DeterministicStateOracle
```


## <a name="input"></a><span data-ttu-id="48f51-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="48f51-106">Input</span></span>

### <a name="idxflagqubit--int"></a><span data-ttu-id="48f51-107">idxflagqubit: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="48f51-107">idxFlagQubit : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="48f51-108">Der Index für das Flag-Qubit des `stateOracle` $A $, das explizit für zwei Register agiert: das Flag $f $ und das System $s $, z. b. $A \ket {0} \_ f\ket {\ PSI} \_ s $.</span><span class="sxs-lookup"><span data-stu-id="48f51-108">The index to the flag qubit of the `stateOracle` $A$, which explicitly acts on two registers: the flag $f$ and the system $s$, e.g. $A\ket{0}\_f\ket{\psi}\_s$.</span></span>


### <a name="stateoracle--stateoracle"></a><span data-ttu-id="48f51-109">stateoracle: [stateoracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span><span class="sxs-lookup"><span data-stu-id="48f51-109">stateOracle : [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span></span>

<span data-ttu-id="48f51-110">Ein Status Vorbereitungs-Oracle $A $ vom Typ `StateOracle` .</span><span class="sxs-lookup"><span data-stu-id="48f51-110">A state preparation oracle $A$ of type `StateOracle`.</span></span>



## <a name="output--deterministicstateoracle"></a><span data-ttu-id="48f51-111">Ausgabe: [deterministicstateoracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span><span class="sxs-lookup"><span data-stu-id="48f51-111">Output : [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span></span>

<span data-ttu-id="48f51-112">Die gleiche Zustands Vorbereitung ist Oracle $A $, aber jetzt vom Typ `DeterministicStateOracle` , sodass Sie auf ein Register angewendet wird, bei dem $a, s $ nicht mehr explizit getrennt werden, z. b.  $A \ket{0\psi} \_ {As} $.</span><span class="sxs-lookup"><span data-stu-id="48f51-112">The same state preparation oracle $A$, but now of type `DeterministicStateOracle`, so it acts on a register where $a,s$ no longer explicitly separate, e.g.  $A\ket{0\psi}\_{as}$.</span></span>

## <a name="see-also"></a><span data-ttu-id="48f51-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="48f51-113">See Also</span></span>

- [<span data-ttu-id="48f51-114">Microsoft. Quantum. Oracles. stateoracle</span><span class="sxs-lookup"><span data-stu-id="48f51-114">Microsoft.Quantum.Oracles.StateOracle</span></span>](xref:Microsoft.Quantum.Oracles.StateOracle)
- [<span data-ttu-id="48f51-115">Microsoft. Quantum. Oracles. deterministicstateoracle</span><span class="sxs-lookup"><span data-stu-id="48f51-115">Microsoft.Quantum.Oracles.DeterministicStateOracle</span></span>](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)
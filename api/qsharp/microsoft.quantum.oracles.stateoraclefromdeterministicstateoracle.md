---
uid: Microsoft.Quantum.Oracles.StateOracleFromDeterministicStateOracle
title: Stateoraclefromdeterministicstateoracle-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: StateOracleFromDeterministicStateOracle
qsharp.summary: Converts an oracle of type `DeterministicStateOracle` to `StateOracle`.
ms.openlocfilehash: 4eed29072cab9e8c106509a6a114c8a071441079
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842504"
---
# <a name="stateoraclefromdeterministicstateoracle-function"></a><span data-ttu-id="72e5c-102">Stateoraclefromdeterministicstateoracle-Funktion</span><span class="sxs-lookup"><span data-stu-id="72e5c-102">StateOracleFromDeterministicStateOracle function</span></span>

<span data-ttu-id="72e5c-103">Namespace: [Microsoft. Quantum. Oracles](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="72e5c-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="72e5c-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="72e5c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="72e5c-105">Konvertiert ein Oracle vom Typ `DeterministicStateOracle` in `StateOracle` .</span><span class="sxs-lookup"><span data-stu-id="72e5c-105">Converts an oracle of type `DeterministicStateOracle` to `StateOracle`.</span></span>

```qsharp
function StateOracleFromDeterministicStateOracle (deterministicStateOracle : Microsoft.Quantum.Oracles.DeterministicStateOracle) : Microsoft.Quantum.Oracles.StateOracle
```


## <a name="input"></a><span data-ttu-id="72e5c-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="72e5c-106">Input</span></span>

### <a name="deterministicstateoracle--deterministicstateoracle"></a><span data-ttu-id="72e5c-107">deterministicstateoracle: [deterministicstateoracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span><span class="sxs-lookup"><span data-stu-id="72e5c-107">deterministicStateOracle : [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span></span>

<span data-ttu-id="72e5c-108">Ein Status Vorbereitungs-Oracle $A $ vom Typ `DeterministicStateOracle` .</span><span class="sxs-lookup"><span data-stu-id="72e5c-108">A state preparation oracle $A$ of type `DeterministicStateOracle`.</span></span>



## <a name="output--stateoracle"></a><span data-ttu-id="72e5c-109">Ausgabe: [stateoracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span><span class="sxs-lookup"><span data-stu-id="72e5c-109">Output : [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span></span>

<span data-ttu-id="72e5c-110">Das gleiche Zustands Vorbereitungs-Oracle $A $, aber jetzt vom Typ `StateOracle` .</span><span class="sxs-lookup"><span data-stu-id="72e5c-110">The same state preparation oracle $A$, but now of type `StateOracle`.</span></span> <span data-ttu-id="72e5c-111">Beachten Sie, dass der FlagIndex in dieser `StateOracle` eine Dummyvariable ist und keine Auswirkung hat.</span><span class="sxs-lookup"><span data-stu-id="72e5c-111">Note that the flag index in this `StateOracle` is a dummy variable and has no effect.</span></span>

## <a name="see-also"></a><span data-ttu-id="72e5c-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="72e5c-112">See Also</span></span>

- [<span data-ttu-id="72e5c-113">Microsoft. Quantum. Oracles. deterministicstateoracle</span><span class="sxs-lookup"><span data-stu-id="72e5c-113">Microsoft.Quantum.Oracles.DeterministicStateOracle</span></span>](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)
- [<span data-ttu-id="72e5c-114">Microsoft. Quantum. Oracles. stateoracle</span><span class="sxs-lookup"><span data-stu-id="72e5c-114">Microsoft.Quantum.Oracles.StateOracle</span></span>](xref:Microsoft.Quantum.Oracles.StateOracle)
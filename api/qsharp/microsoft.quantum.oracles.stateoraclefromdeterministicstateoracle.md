---
uid: Microsoft.Quantum.Oracles.StateOracleFromDeterministicStateOracle
title: Stateoraclefromdeterministicstateoracle-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: StateOracleFromDeterministicStateOracle
qsharp.summary: Converts an oracle of type `DeterministicStateOracle` to `StateOracle`.
ms.openlocfilehash: ccb083dbaaec2f306ba0740ef364ebb22408ed98
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724221"
---
# <a name="stateoraclefromdeterministicstateoracle-function"></a><span data-ttu-id="056b1-102">Stateoraclefromdeterministicstateoracle-Funktion</span><span class="sxs-lookup"><span data-stu-id="056b1-102">StateOracleFromDeterministicStateOracle function</span></span>

<span data-ttu-id="056b1-103">Namespace: [Microsoft. Quantum. Oracles](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="056b1-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="056b1-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="056b1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="056b1-105">Konvertiert ein Oracle vom Typ `DeterministicStateOracle` in `StateOracle` .</span><span class="sxs-lookup"><span data-stu-id="056b1-105">Converts an oracle of type `DeterministicStateOracle` to `StateOracle`.</span></span>

```qsharp
function StateOracleFromDeterministicStateOracle (deterministicStateOracle : Microsoft.Quantum.Oracles.DeterministicStateOracle) : Microsoft.Quantum.Oracles.StateOracle
```


## <a name="input"></a><span data-ttu-id="056b1-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="056b1-106">Input</span></span>

### <a name="deterministicstateoracle--deterministicstateoracle"></a><span data-ttu-id="056b1-107">deterministicstateoracle: [deterministicstateoracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span><span class="sxs-lookup"><span data-stu-id="056b1-107">deterministicStateOracle : [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span></span>

<span data-ttu-id="056b1-108">Ein Status Vorbereitungs-Oracle $A $ vom Typ `DeterministicStateOracle` .</span><span class="sxs-lookup"><span data-stu-id="056b1-108">A state preparation oracle $A$ of type `DeterministicStateOracle`.</span></span>



## <a name="output--stateoracle"></a><span data-ttu-id="056b1-109">Ausgabe: [stateoracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span><span class="sxs-lookup"><span data-stu-id="056b1-109">Output : [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span></span>

<span data-ttu-id="056b1-110">Das gleiche Zustands Vorbereitungs-Oracle $A $, aber jetzt vom Typ `StateOracle` .</span><span class="sxs-lookup"><span data-stu-id="056b1-110">The same state preparation oracle $A$, but now of type `StateOracle`.</span></span> <span data-ttu-id="056b1-111">Beachten Sie, dass der FlagIndex in dieser `StateOracle` eine Dummyvariable ist und keine Auswirkung hat.</span><span class="sxs-lookup"><span data-stu-id="056b1-111">Note that the flag index in this `StateOracle` is a dummy variable and has no effect.</span></span>

## <a name="see-also"></a><span data-ttu-id="056b1-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="056b1-112">See Also</span></span>

- [<span data-ttu-id="056b1-113">Microsoft. Quantum. Oracles. deterministicstateoracle</span><span class="sxs-lookup"><span data-stu-id="056b1-113">Microsoft.Quantum.Oracles.DeterministicStateOracle</span></span>](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)
- [<span data-ttu-id="056b1-114">Microsoft. Quantum. Oracles. stateoracle</span><span class="sxs-lookup"><span data-stu-id="056b1-114">Microsoft.Quantum.Oracles.StateOracle</span></span>](xref:Microsoft.Quantum.Oracles.StateOracle)
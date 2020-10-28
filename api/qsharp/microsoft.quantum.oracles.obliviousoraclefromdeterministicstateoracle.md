---
uid: Microsoft.Quantum.Oracles.ObliviousOracleFromDeterministicStateOracle
title: Obliviousoraclefromdeterministicstateoracle-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ObliviousOracleFromDeterministicStateOracle
qsharp.summary: Combines the oracles `DeterministicStateOracle` and `ObliviousOracle`.
ms.openlocfilehash: 9e18776ad4d6adf0068213117c6d1d8ed5c5f126
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722220"
---
# <a name="obliviousoraclefromdeterministicstateoracle-function"></a><span data-ttu-id="65f15-102">Obliviousoraclefromdeterministicstateoracle-Funktion</span><span class="sxs-lookup"><span data-stu-id="65f15-102">ObliviousOracleFromDeterministicStateOracle function</span></span>

<span data-ttu-id="65f15-103">Namespace: [Microsoft. Quantum. Oracles](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="65f15-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="65f15-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="65f15-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="65f15-105">Kombiniert die Oracles `DeterministicStateOracle` und `ObliviousOracle` .</span><span class="sxs-lookup"><span data-stu-id="65f15-105">Combines the oracles `DeterministicStateOracle` and `ObliviousOracle`.</span></span>

```qsharp
function ObliviousOracleFromDeterministicStateOracle (ancillaOracle : Microsoft.Quantum.Oracles.DeterministicStateOracle, signalOracle : Microsoft.Quantum.Oracles.ObliviousOracle) : Microsoft.Quantum.Oracles.ObliviousOracle
```


## <a name="input"></a><span data-ttu-id="65f15-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="65f15-106">Input</span></span>

### <a name="ancillaoracle--deterministicstateoracle"></a><span data-ttu-id="65f15-107">"ancillaoracle: [deterministicstateoracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle) "</span><span class="sxs-lookup"><span data-stu-id="65f15-107">ancillaOracle : [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span></span>

<span data-ttu-id="65f15-108">Ein Status Vorbereitungs-Oracle-$A $ vom Typ, der `DeterministicStateOracle` für Register $a $ fungiert.</span><span class="sxs-lookup"><span data-stu-id="65f15-108">A state preparation oracle $A$ of type `DeterministicStateOracle` acting on register $a$.</span></span>


### <a name="signaloracle--obliviousoracle"></a><span data-ttu-id="65f15-109">signaloracle: [obliviousoracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span><span class="sxs-lookup"><span data-stu-id="65f15-109">signalOracle : [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span></span>

<span data-ttu-id="65f15-110">Ein Oracle-$U $ vom Typ `ObliviousOracle` , der gemeinsam für Register $a, s $, verhält.</span><span class="sxs-lookup"><span data-stu-id="65f15-110">A oracle $U$ of type `ObliviousOracle` acting jointly on register $a,s$.</span></span>



## <a name="output--obliviousoracle"></a><span data-ttu-id="65f15-111">Ausgabe: [obliviousoracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span><span class="sxs-lookup"><span data-stu-id="65f15-111">Output : [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span></span>

<span data-ttu-id="65f15-112">Ein Oracle-$O = UA $ vom Typ `ObliviousOracle` .</span><span class="sxs-lookup"><span data-stu-id="65f15-112">An oracle $O=UA$ of type `ObliviousOracle`.</span></span>

## <a name="see-also"></a><span data-ttu-id="65f15-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="65f15-113">See Also</span></span>

- [<span data-ttu-id="65f15-114">Microsoft. Quantum. Oracles. deterministicstateoracle</span><span class="sxs-lookup"><span data-stu-id="65f15-114">Microsoft.Quantum.Oracles.DeterministicStateOracle</span></span>](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)
- [<span data-ttu-id="65f15-115">Microsoft. Quantum. Oracles. schräviousoracle</span><span class="sxs-lookup"><span data-stu-id="65f15-115">Microsoft.Quantum.Oracles.ObliviousOracle</span></span>](xref:Microsoft.Quantum.Oracles.ObliviousOracle)
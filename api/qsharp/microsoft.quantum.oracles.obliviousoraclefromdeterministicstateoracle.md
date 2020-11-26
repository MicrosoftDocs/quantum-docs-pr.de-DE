---
uid: Microsoft.Quantum.Oracles.ObliviousOracleFromDeterministicStateOracle
title: Obliviousoraclefromdeterministicstateoracle-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ObliviousOracleFromDeterministicStateOracle
qsharp.summary: Combines the oracles `DeterministicStateOracle` and `ObliviousOracle`.
ms.openlocfilehash: 8f1fe34e38edefba228fb9d01e1712e4c0916970
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226688"
---
# <a name="obliviousoraclefromdeterministicstateoracle-function"></a><span data-ttu-id="751ea-102">Obliviousoraclefromdeterministicstateoracle-Funktion</span><span class="sxs-lookup"><span data-stu-id="751ea-102">ObliviousOracleFromDeterministicStateOracle function</span></span>

<span data-ttu-id="751ea-103">Namespace: [Microsoft. Quantum. Oracles](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="751ea-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="751ea-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="751ea-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="751ea-105">Kombiniert die Oracles `DeterministicStateOracle` und `ObliviousOracle` .</span><span class="sxs-lookup"><span data-stu-id="751ea-105">Combines the oracles `DeterministicStateOracle` and `ObliviousOracle`.</span></span>

```qsharp
function ObliviousOracleFromDeterministicStateOracle (ancillaOracle : Microsoft.Quantum.Oracles.DeterministicStateOracle, signalOracle : Microsoft.Quantum.Oracles.ObliviousOracle) : Microsoft.Quantum.Oracles.ObliviousOracle
```


## <a name="input"></a><span data-ttu-id="751ea-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="751ea-106">Input</span></span>

### <a name="ancillaoracle--deterministicstateoracle"></a><span data-ttu-id="751ea-107">"ancillaoracle: [deterministicstateoracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle) "</span><span class="sxs-lookup"><span data-stu-id="751ea-107">ancillaOracle : [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span></span>

<span data-ttu-id="751ea-108">Ein Status Vorbereitungs-Oracle-$A $ vom Typ, der `DeterministicStateOracle` für Register $a $ fungiert.</span><span class="sxs-lookup"><span data-stu-id="751ea-108">A state preparation oracle $A$ of type `DeterministicStateOracle` acting on register $a$.</span></span>


### <a name="signaloracle--obliviousoracle"></a><span data-ttu-id="751ea-109">signaloracle: [obliviousoracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span><span class="sxs-lookup"><span data-stu-id="751ea-109">signalOracle : [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span></span>

<span data-ttu-id="751ea-110">Ein Oracle-$U $ vom Typ `ObliviousOracle` , der gemeinsam für Register $a, s $, verhält.</span><span class="sxs-lookup"><span data-stu-id="751ea-110">A oracle $U$ of type `ObliviousOracle` acting jointly on register $a,s$.</span></span>



## <a name="output--obliviousoracle"></a><span data-ttu-id="751ea-111">Ausgabe: [obliviousoracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span><span class="sxs-lookup"><span data-stu-id="751ea-111">Output : [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span></span>

<span data-ttu-id="751ea-112">Ein Oracle-$O = UA $ vom Typ `ObliviousOracle` .</span><span class="sxs-lookup"><span data-stu-id="751ea-112">An oracle $O=UA$ of type `ObliviousOracle`.</span></span>

## <a name="see-also"></a><span data-ttu-id="751ea-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="751ea-113">See Also</span></span>

- [<span data-ttu-id="751ea-114">Microsoft. Quantum. Oracles. deterministicstateoracle</span><span class="sxs-lookup"><span data-stu-id="751ea-114">Microsoft.Quantum.Oracles.DeterministicStateOracle</span></span>](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)
- [<span data-ttu-id="751ea-115">Microsoft. Quantum. Oracles. schräviousoracle</span><span class="sxs-lookup"><span data-stu-id="751ea-115">Microsoft.Quantum.Oracles.ObliviousOracle</span></span>](xref:Microsoft.Quantum.Oracles.ObliviousOracle)
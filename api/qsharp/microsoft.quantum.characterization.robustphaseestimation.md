---
uid: Microsoft.Quantum.Characterization.RobustPhaseEstimation
title: RobustPhaseEstimation-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: RobustPhaseEstimation
qsharp.summary: Performs the robust non-iterative quantum phase estimation algorithm for a given oracle `U` and eigenstate, and provides a single real-valued estimate of the phase with variance scaling at the Heisenberg limit.
ms.openlocfilehash: 3e6774e2fe348668840cdc08fe3a070ec3d82a6d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216080"
---
# <a name="robustphaseestimation-operation"></a><span data-ttu-id="b7bbe-102">RobustPhaseEstimation-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b7bbe-102">RobustPhaseEstimation operation</span></span>

<span data-ttu-id="b7bbe-103">Namespace: [Microsoft. Quantum. Charakterisierung](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="b7bbe-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="b7bbe-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b7bbe-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b7bbe-105">Führt den robusten, nicht iterativen Quantum-Phasen-Schätz Algorithmus für ein bestimmtes Oracle `U` und einen eigen Zustand aus und bietet eine einzelne, in Echtzeit angegebene Schätzung der Phase mit Varianz Skalierung am Heisenberg-Limit.</span><span class="sxs-lookup"><span data-stu-id="b7bbe-105">Performs the robust non-iterative quantum phase estimation algorithm for a given oracle `U` and eigenstate, and provides a single real-valued estimate of the phase with variance scaling at the Heisenberg limit.</span></span>

```qsharp
operation RobustPhaseEstimation (bitsPrecision : Int, oracle : Microsoft.Quantum.Oracles.DiscreteOracle, targetState : Qubit[]) : Double
```


## <a name="input"></a><span data-ttu-id="b7bbe-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b7bbe-106">Input</span></span>

### <a name="bitsprecision--int"></a><span data-ttu-id="b7bbe-107">bitationcision: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b7bbe-107">bitsPrecision : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b7bbe-108">Dies bietet eine Schätzung von $ \phi $ mit der Standardabweichung $ \sigma \le 2 \ Pi/2 ^ \text{bitspcision} $, wobei eine Reihe von Abfragen skaliert wird, wie z. b. $ \sigma \le 10,7 \pi/\text{# of queries} $.</span><span class="sxs-lookup"><span data-stu-id="b7bbe-108">This provides an estimate of $\phi$ with standard deviation $\sigma \le 2\pi / 2^\text{bitsPrecision}$ using a number of queries scaling like $\sigma \le 10.7 \pi / \text{# of queries}$.</span></span>


### <a name="oracle--discreteoracle"></a><span data-ttu-id="b7bbe-109">Oracle: [diskreteoracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span><span class="sxs-lookup"><span data-stu-id="b7bbe-109">oracle : [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span></span>

<span data-ttu-id="b7bbe-110">Ein Vorgang, der $U ^ m $ für angegebene ganzzahlige $m $ implementiert.</span><span class="sxs-lookup"><span data-stu-id="b7bbe-110">An operation implementing $U^m$ for given integer powers $m$.</span></span>


### <a name="targetstate--qubit"></a><span data-ttu-id="b7bbe-111">targetState: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="b7bbe-111">targetState : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="b7bbe-112">Ein Quantum-Register, für das $U $ agiert.</span><span class="sxs-lookup"><span data-stu-id="b7bbe-112">A quantum register that $U$ acts on.</span></span> <span data-ttu-id="b7bbe-113">Wenn ein eigen Status $ \ket{\phi} $ von $U $ gespeichert wird, $U \ket{\phi} = e ^ {i\phi} \ket{\phi} $ für $ \phi\in (-\pi, \pi] $ eine unbekannte Phase.</span><span class="sxs-lookup"><span data-stu-id="b7bbe-113">If it stores an eigenstate $\ket{\phi}$ of $U$, then $U\ket{\phi} = e^{i\phi} \ket{\phi}$ for $\phi\in(-\pi,\pi]$ an unknown phase.</span></span>



## <a name="output--double"></a><span data-ttu-id="b7bbe-114">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="b7bbe-114">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="remarks"></a><span data-ttu-id="b7bbe-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b7bbe-115">Remarks</span></span>

<span data-ttu-id="b7bbe-116">Der Grenzwert für eine große Anzahl von Abfragen Cramer-Rao unteren Grenzen der geschätzten Schätzung von $ \phi $ entspricht $ \sigma \ge 2 \pi/\text{# of queries} $.</span><span class="sxs-lookup"><span data-stu-id="b7bbe-116">In the limit of a large number of queries, Cramer-Rao lower bounds for the standard deviation of the estimate of $\phi$ satisfy $\sigma \ge 2 \pi / \text{# of queries}$.</span></span>

## <a name="references"></a><span data-ttu-id="b7bbe-117">Referenzen</span><span class="sxs-lookup"><span data-stu-id="b7bbe-117">References</span></span>

- <span data-ttu-id="b7bbe-118">Robuste Kalibrierung eines universellen Single-Qubit Gate-Set über die robuste Phasen Schätzung Shelby Kimmel, Guang Hao Low, Theodore J. Yoder https://arxiv.org/abs/1502.02677</span><span class="sxs-lookup"><span data-stu-id="b7bbe-118">Robust Calibration of a Universal Single-Qubit Gate-Set via Robust Phase Estimation Shelby Kimmel, Guang Hao Low, Theodore J. Yoder https://arxiv.org/abs/1502.02677</span></span>
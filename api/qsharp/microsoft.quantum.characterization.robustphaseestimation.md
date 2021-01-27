---
uid: Microsoft.Quantum.Characterization.RobustPhaseEstimation
title: RobustPhaseEstimation-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: RobustPhaseEstimation
qsharp.summary: Performs the robust non-iterative quantum phase estimation algorithm for a given oracle `U` and eigenstate, and provides a single real-valued estimate of the phase with variance scaling at the Heisenberg limit.
ms.openlocfilehash: 4b37c8275a5b2aee8534bacc5831281aa498b57d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851802"
---
# <a name="robustphaseestimation-operation"></a><span data-ttu-id="a41dd-102">RobustPhaseEstimation-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a41dd-102">RobustPhaseEstimation operation</span></span>

<span data-ttu-id="a41dd-103">Namespace: [Microsoft. Quantum. Charakterisierung](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="a41dd-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="a41dd-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a41dd-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a41dd-105">Führt den robusten, nicht iterativen Quantum-Phasen-Schätz Algorithmus für ein bestimmtes Oracle `U` und einen eigen Zustand aus und bietet eine einzelne, in Echtzeit angegebene Schätzung der Phase mit Varianz Skalierung am Heisenberg-Limit.</span><span class="sxs-lookup"><span data-stu-id="a41dd-105">Performs the robust non-iterative quantum phase estimation algorithm for a given oracle `U` and eigenstate, and provides a single real-valued estimate of the phase with variance scaling at the Heisenberg limit.</span></span>

```qsharp
operation RobustPhaseEstimation (bitsPrecision : Int, oracle : Microsoft.Quantum.Oracles.DiscreteOracle, targetState : Qubit[]) : Double
```


## <a name="input"></a><span data-ttu-id="a41dd-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a41dd-106">Input</span></span>

### <a name="bitsprecision--int"></a><span data-ttu-id="a41dd-107">bitationcision: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a41dd-107">bitsPrecision : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a41dd-108">Dies bietet eine Schätzung von $ \phi $ mit der Standardabweichung $ \sigma \le 2 \ Pi/2 ^ \text{bitspcision} $, wobei eine Reihe von Abfragen skaliert wird, wie z. b. $ \sigma \le 10,7 \pi/\text{# of queries} $.</span><span class="sxs-lookup"><span data-stu-id="a41dd-108">This provides an estimate of $\phi$ with standard deviation $\sigma \le 2\pi / 2^\text{bitsPrecision}$ using a number of queries scaling like $\sigma \le 10.7 \pi / \text{# of queries}$.</span></span>


### <a name="oracle--discreteoracle"></a><span data-ttu-id="a41dd-109">Oracle: [diskreteoracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span><span class="sxs-lookup"><span data-stu-id="a41dd-109">oracle : [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span></span>

<span data-ttu-id="a41dd-110">Ein Vorgang, der $U ^ m $ für angegebene ganzzahlige $m $ implementiert.</span><span class="sxs-lookup"><span data-stu-id="a41dd-110">An operation implementing $U^m$ for given integer powers $m$.</span></span>


### <a name="targetstate--qubit"></a><span data-ttu-id="a41dd-111">targetState: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="a41dd-111">targetState : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="a41dd-112">Ein Quantum-Register, für das $U $ agiert.</span><span class="sxs-lookup"><span data-stu-id="a41dd-112">A quantum register that $U$ acts on.</span></span> <span data-ttu-id="a41dd-113">Wenn ein eigen Status $ \ket{\phi} $ von $U $ gespeichert wird, $U \ket{\phi} = e ^ {i\phi} \ket{\phi} $ für $ \phi\in (-\pi, \pi] $ eine unbekannte Phase.</span><span class="sxs-lookup"><span data-stu-id="a41dd-113">If it stores an eigenstate $\ket{\phi}$ of $U$, then $U\ket{\phi} = e^{i\phi} \ket{\phi}$ for $\phi\in(-\pi,\pi]$ an unknown phase.</span></span>



## <a name="output--double"></a><span data-ttu-id="a41dd-114">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="a41dd-114">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="remarks"></a><span data-ttu-id="a41dd-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a41dd-115">Remarks</span></span>

<span data-ttu-id="a41dd-116">Der Grenzwert für eine große Anzahl von Abfragen Cramer-Rao unteren Grenzen der geschätzten Schätzung von $ \phi $ entspricht $ \sigma \ge 2 \pi/\text{# of queries} $.</span><span class="sxs-lookup"><span data-stu-id="a41dd-116">In the limit of a large number of queries, Cramer-Rao lower bounds for the standard deviation of the estimate of $\phi$ satisfy $\sigma \ge 2 \pi / \text{# of queries}$.</span></span>

## <a name="references"></a><span data-ttu-id="a41dd-117">References</span><span class="sxs-lookup"><span data-stu-id="a41dd-117">References</span></span>

- <span data-ttu-id="a41dd-118">Robuste Kalibrierung eines universellen Single-Qubit Gate-Set über die robuste Phasen Schätzung Shelby Kimmel, Guang Hao Low, Theodore J. Yoder https://arxiv.org/abs/1502.02677</span><span class="sxs-lookup"><span data-stu-id="a41dd-118">Robust Calibration of a Universal Single-Qubit Gate-Set via Robust Phase Estimation Shelby Kimmel, Guang Hao Low, Theodore J. Yoder https://arxiv.org/abs/1502.02677</span></span>
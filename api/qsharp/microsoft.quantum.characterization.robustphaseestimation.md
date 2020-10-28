---
uid: Microsoft.Quantum.Characterization.RobustPhaseEstimation
title: RobustPhaseEstimation-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: RobustPhaseEstimation
qsharp.summary: Performs the robust non-iterative quantum phase estimation algorithm for a given oracle `U` and eigenstate, and provides a single real-valued estimate of the phase with variance scaling at the Heisenberg limit.
ms.openlocfilehash: d04ee578c0e6f916e9a4da451075b79e0630c70a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703596"
---
# <a name="robustphaseestimation-operation"></a><span data-ttu-id="29b34-102">RobustPhaseEstimation-Vorgang</span><span class="sxs-lookup"><span data-stu-id="29b34-102">RobustPhaseEstimation operation</span></span>

<span data-ttu-id="29b34-103">Namespace: [Microsoft. Quantum. Charakterisierung](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="29b34-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="29b34-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="29b34-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="29b34-105">Führt den robusten, nicht iterativen Quantum-Phasen-Schätz Algorithmus für ein bestimmtes Oracle `U` und einen eigen Zustand aus und bietet eine einzelne, in Echtzeit angegebene Schätzung der Phase mit Varianz Skalierung am Heisenberg-Limit.</span><span class="sxs-lookup"><span data-stu-id="29b34-105">Performs the robust non-iterative quantum phase estimation algorithm for a given oracle `U` and eigenstate, and provides a single real-valued estimate of the phase with variance scaling at the Heisenberg limit.</span></span>

```qsharp
operation RobustPhaseEstimation (bitsPrecision : Int, oracle : Microsoft.Quantum.Oracles.DiscreteOracle, targetState : Qubit[]) : Double
```


## <a name="input"></a><span data-ttu-id="29b34-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="29b34-106">Input</span></span>

### <a name="bitsprecision--int"></a><span data-ttu-id="29b34-107">bitationcision: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="29b34-107">bitsPrecision : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="29b34-108">Dies bietet eine Schätzung von $ \phi $ mit der Standardabweichung $ \sigma \le 2 \ Pi/2 ^ \text{bitspcision} $, wobei eine Reihe von Abfragen skaliert wird, wie z. b. $ \sigma \le 10,7 \pi/\text{# of queries} $.</span><span class="sxs-lookup"><span data-stu-id="29b34-108">This provides an estimate of $\phi$ with standard deviation $\sigma \le 2\pi / 2^\text{bitsPrecision}$ using a number of queries scaling like $\sigma \le 10.7 \pi / \text{# of queries}$.</span></span>


### <a name="oracle--discreteoracle"></a><span data-ttu-id="29b34-109">Oracle: [diskreteoracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span><span class="sxs-lookup"><span data-stu-id="29b34-109">oracle : [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span></span>

<span data-ttu-id="29b34-110">Ein Vorgang, der $U ^ m $ für angegebene ganzzahlige $m $ implementiert.</span><span class="sxs-lookup"><span data-stu-id="29b34-110">An operation implementing $U^m$ for given integer powers $m$.</span></span>


### <a name="targetstate--qubit"></a><span data-ttu-id="29b34-111">targetState: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="29b34-111">targetState : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="29b34-112">Ein Quantum-Register, für das $U $ agiert.</span><span class="sxs-lookup"><span data-stu-id="29b34-112">A quantum register that $U$ acts on.</span></span> <span data-ttu-id="29b34-113">Wenn ein eigen Status $ \ket{\phi} $ von $U $ gespeichert wird, $U \ket{\phi} = e ^ {i\phi} \ket{\phi} $ für $ \phi\in (-\pi, \pi] $ eine unbekannte Phase.</span><span class="sxs-lookup"><span data-stu-id="29b34-113">If it stores an eigenstate $\ket{\phi}$ of $U$, then $U\ket{\phi} = e^{i\phi} \ket{\phi}$ for $\phi\in(-\pi,\pi]$ an unknown phase.</span></span>



## <a name="output--double"></a><span data-ttu-id="29b34-114">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="29b34-114">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="remarks"></a><span data-ttu-id="29b34-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="29b34-115">Remarks</span></span>

<span data-ttu-id="29b34-116">Der Grenzwert für eine große Anzahl von Abfragen Cramer-Rao unteren Grenzen der geschätzten Schätzung von $ \phi $ entspricht $ \sigma \ge 2 \pi/\text{# of queries} $.</span><span class="sxs-lookup"><span data-stu-id="29b34-116">In the limit of a large number of queries, Cramer-Rao lower bounds for the standard deviation of the estimate of $\phi$ satisfy $\sigma \ge 2 \pi / \text{# of queries}$.</span></span>

## <a name="references"></a><span data-ttu-id="29b34-117">Referenzen</span><span class="sxs-lookup"><span data-stu-id="29b34-117">References</span></span>

- <span data-ttu-id="29b34-118">Robuste Kalibrierung eines universellen Single-Qubit Gate-Set über die robuste Phasen Schätzung Shelby Kimmel, Guang Hao Low, Theodore J. Yoder https://arxiv.org/abs/1502.02677</span><span class="sxs-lookup"><span data-stu-id="29b34-118">Robust Calibration of a Universal Single-Qubit Gate-Set via Robust Phase Estimation Shelby Kimmel, Guang Hao Low, Theodore J. Yoder https://arxiv.org/abs/1502.02677</span></span>
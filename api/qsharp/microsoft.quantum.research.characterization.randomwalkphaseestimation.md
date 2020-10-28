---
uid: Microsoft.Quantum.Research.Characterization.RandomWalkPhaseEstimation
title: Randomwalkphaseschätzungsvorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Characterization
qsharp.name: RandomWalkPhaseEstimation
qsharp.summary: Performs iterative phase estimation using a random walk to approximate Bayesian inference on the classical measurement results from a given oracle and eigenstate.
ms.openlocfilehash: 5e0c0871b916ff51b85dec8703111788b5204bc6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701856"
---
# <a name="randomwalkphaseestimation-operation"></a><span data-ttu-id="c7162-102">Randomwalkphaseschätzungsvorgang</span><span class="sxs-lookup"><span data-stu-id="c7162-102">RandomWalkPhaseEstimation operation</span></span>

<span data-ttu-id="c7162-103">Namespace: [Microsoft. Quantum. Research. Charakterisierung](xref:Microsoft.Quantum.Research.Characterization)</span><span class="sxs-lookup"><span data-stu-id="c7162-103">Namespace: [Microsoft.Quantum.Research.Characterization](xref:Microsoft.Quantum.Research.Characterization)</span></span>

<span data-ttu-id="c7162-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c7162-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c7162-105">Führt eine iterative Phasen Schätzung mithilfe eines zufälligen Durchlaufs aus, um einen ungefähren bayesschen Rückschluss auf die klassischen Messergebnisse eines bestimmten Oracle-und eigen Zustands festzustellen.</span><span class="sxs-lookup"><span data-stu-id="c7162-105">Performs iterative phase estimation using a random walk to approximate Bayesian inference on the classical measurement results from a given oracle and eigenstate.</span></span>

```qsharp
operation RandomWalkPhaseEstimation (initialMean : Double, initialStdDev : Double, nMeasurements : Int, maxMeasurements : Int, unwind : Int, oracle : Microsoft.Quantum.Oracles.ContinuousOracle, targetState : Qubit[]) : Double
```


## <a name="input"></a><span data-ttu-id="c7162-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c7162-106">Input</span></span>

### <a name="initialmean--double"></a><span data-ttu-id="c7162-107">initialmean: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="c7162-107">initialMean : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="c7162-108">Mittelwert der anfänglichen normalen Vorverteilung über $ \phi $.</span><span class="sxs-lookup"><span data-stu-id="c7162-108">Mean of the initial normal prior distribution over $\phi$.</span></span>


### <a name="initialstddev--double"></a><span data-ttu-id="c7162-109">initialstddev: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="c7162-109">initialStdDev : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="c7162-110">Standard Abweichung der anfänglichen normalen früheren Verteilung über $ \phi $.</span><span class="sxs-lookup"><span data-stu-id="c7162-110">Standard deviation of the initial normal prior distribution over $\phi$.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="c7162-111">nmessungen: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c7162-111">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c7162-112">Anzahl der Messungen, die in der abschließenden nach-unten-Schätzung akzeptiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c7162-112">Number of measurements to be accepted into the final posterior estimate.</span></span>


### <a name="maxmeasurements--int"></a><span data-ttu-id="c7162-113">maxmessungen: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c7162-113">maxMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c7162-114">Die Gesamtanzahl der Messungen, die durchgeführt werden können, bevor der Vorgang als fehlgeschlagen eingestuft wird.</span><span class="sxs-lookup"><span data-stu-id="c7162-114">Total number of measurements than can be taken before the operation is considered to have failed.</span></span>


### <a name="unwind--int"></a><span data-ttu-id="c7162-115">entladen: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c7162-115">unwind : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c7162-116">Anzahl der zu debuggende Ergebnisse, wenn Konsistenzprüfungen fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="c7162-116">Number of results to forget when consistency checks fail.</span></span>


### <a name="oracle--continuousoracle"></a><span data-ttu-id="c7162-117">Oracle: [continuousoracle](xref:Microsoft.Quantum.Oracles.ContinuousOracle)</span><span class="sxs-lookup"><span data-stu-id="c7162-117">oracle : [ContinuousOracle](xref:Microsoft.Quantum.Oracles.ContinuousOracle)</span></span>

<span data-ttu-id="c7162-118">Ein Vorgang, der eine einheitliche $U $ darstellt, sodass $U (t) \ket{\phi} = e ^ {i t \phi}\ket{\phi} $ für Eigen Zustände $ \ket{\phi} $ mit unbekannter Phase $ \phi \ in \mathbb{r} ^ + $.</span><span class="sxs-lookup"><span data-stu-id="c7162-118">An operation representing a unitary $U$ such that $U(t)\ket{\phi} = e^{i t \phi}\ket{\phi}$ for eigenstates $\ket{\phi}$ with unknown phase $\phi \in \mathbb{R}^+$.</span></span>


### <a name="targetstate--qubit"></a><span data-ttu-id="c7162-119">targetState: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="c7162-119">targetState : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="c7162-120">Ein Register, für das $U $ agiert.</span><span class="sxs-lookup"><span data-stu-id="c7162-120">A register that $U$ acts on.</span></span>



## <a name="output--double"></a><span data-ttu-id="c7162-121">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="c7162-121">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="c7162-122">Die letzte Schätzung $ \hat{\phi} \mathrel{: =} \expect [\phi] $, bei der die Annahme über dem Posterior mit allen akzeptierten Daten liegt.</span><span class="sxs-lookup"><span data-stu-id="c7162-122">The final estimate $\hat{\phi} \mathrel{:=} \expect[\phi]$ , where the expectation is over the posterior given all accepted data.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7162-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c7162-123">Remarks</span></span>

### <a name="iterative-phase-estimation-and-eigenstates"></a><span data-ttu-id="c7162-124">Iterative Phasen Schätzung und eigen Zustände</span><span class="sxs-lookup"><span data-stu-id="c7162-124">Iterative Phase Estimation and Eigenstates</span></span>

<span data-ttu-id="c7162-125">Im Allgemeinen muss das Eingabe Register `eigenstate` nicht den eigen Zustand $ \ket{\phi} $ von $U $ aufweisen, kann jedoch eine übergeordnete Position gegenüber eigen Zuständen sein.</span><span class="sxs-lookup"><span data-stu-id="c7162-125">In general, the input register `eigenstate` need not be an eigenstate $\ket{\phi}$ of $U$, but can be a superposition over eigenstates.</span></span> <span data-ttu-id="c7162-126">Angenommen, der Eingabe Zustand wird von \begin{align} \ket{\psi} & = \sum \_ {j} \alpha \_ j \ket{\phi \_ j} angegeben. \end{align}, wobei "$ \{ \alpha \_ j $" \} komplexe Koeffizienten wie "$ \sum \_ j | \alpha \_ j | ^ 2 = $1" und "where $U \ket{\phi \_ j} = \phi \_ j\ket {\ Phi \_ j} $" sind.</span><span class="sxs-lookup"><span data-stu-id="c7162-126">Suppose that the input state is given by \begin{align} \ket{\psi} & = \sum\_{j} \alpha\_j \ket{\phi\_j}, \end{align} where $\{\alpha\_j\}$ are complex coefficients such that $\sum\_j |\alpha\_j|^2 = 1$ and where $U\ket{\phi\_j} = \phi\_j\ket{\phi\_j}$.</span></span>

<span data-ttu-id="c7162-127">Anschließend wird die iterative Phasen Schätzung letztendlich in einen einzelnen eigen Zustand konvergiert, wie im [Entwicklungs Handbuch](xref:microsoft.quantum.libraries.characterization#iterative-phase-estimation-without-eigenstates)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c7162-127">Then, performing iterative phase estimation will eventually converge to a single eigenstate, as described in the [development guide](xref:microsoft.quantum.libraries.characterization#iterative-phase-estimation-without-eigenstates).</span></span>

### <a name="experiment-design"></a><span data-ttu-id="c7162-128">Experiment Entwurf</span><span class="sxs-lookup"><span data-stu-id="c7162-128">Experiment Design</span></span>

<span data-ttu-id="c7162-129">Die Messzeiten $t $ und der inversionswinkel $ \an die an über gegebene Daten `oracle` werden gemäß der *Partikel Annahme Heuristik* , \begin{align} \Der Ta \sim \pr (\phi), \quad t \ca \frac {1} {\variance{\phi}}.</span><span class="sxs-lookup"><span data-stu-id="c7162-129">The measurement times $t$ and inversion angles $\theta$ passed to `oracle` are chosen according to the *particle guess heuristic* , \begin{align} \theta \sim \Pr(\phi),\quad t \approx \frac{1}{\variance{\phi}}.</span></span>
<span data-ttu-id="c7162-130">\end{align} diese Heuristik eignet sich optimal, um die erwartete nachträgliche Abweichung in der iterativen Phasen Schätzung unter der Annahme eines normalen vorherigen zu verringern.</span><span class="sxs-lookup"><span data-stu-id="c7162-130">\end{align} This heuristic is optimal for reducing the expected posterior variance in iterative phase estimation under the assumption of a normal prior.</span></span>

### <a name="optimality"></a><span data-ttu-id="c7162-131">Mindestgrößeneinheit</span><span class="sxs-lookup"><span data-stu-id="c7162-131">Optimality</span></span>

<span data-ttu-id="c7162-132">Dieser Vorgang entspricht der optimalen Schätzung für die Phase $ \phi $, die mithilfe des quadratischen Verlusts $L (\phi, \hat{\phi}) \mathrel{: =} (\phi-\hat{\phi}) ^ 2 $ ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="c7162-132">This operation approximates the optimal estimator for the phase $\phi$, as evaluated using the quadratic loss $L(\phi, \hat{\phi}) \mathrel{:=} (\phi - \hat{\phi})^2$.</span></span>

<span data-ttu-id="c7162-133">Weitere Informationen zu den Statistiken der iterativen Phasen Schätzung finden Sie unter [bayyesian-Phasen Schätzung](xref:microsoft.quantum.libraries.characterization#bayesian-phase-estimation) .</span><span class="sxs-lookup"><span data-stu-id="c7162-133">See [Bayesian Phase Estimation](xref:microsoft.quantum.libraries.characterization#bayesian-phase-estimation) for more details on the statistics of iterative phase estimation.</span></span>

## <a name="references"></a><span data-ttu-id="c7162-134">Referenzen</span><span class="sxs-lookup"><span data-stu-id="c7162-134">References</span></span>

- <span data-ttu-id="c7162-135">Ferrie *et al.* 2011 [doi: 10/TFX](https://doi.org/10.1007/s11128-012-0407-6), [arXiv: 1110.3067](https://arxiv.org/abs/1110.3067).</span><span class="sxs-lookup"><span data-stu-id="c7162-135">Ferrie *et al.* 2011 [doi:10/tfx](https://doi.org/10.1007/s11128-012-0407-6), [arXiv:1110.3067](https://arxiv.org/abs/1110.3067).</span></span>
- <span data-ttu-id="c7162-136">Wiebe *et al.* 2013 [doi: 10/TF3](https://doi.org/10.1103/PhysRevLett.112.190501), [arXiv: 1309.0876](https://arxiv.org/abs/1309.0876)</span><span class="sxs-lookup"><span data-stu-id="c7162-136">Wiebe *et al.* 2013 [doi:10/tf3](https://doi.org/10.1103/PhysRevLett.112.190501), [arXiv:1309.0876](https://arxiv.org/abs/1309.0876)</span></span>
- <span data-ttu-id="c7162-137">Wiebe und Granade 2018 *(in Vorbereitung)* .</span><span class="sxs-lookup"><span data-stu-id="c7162-137">Wiebe and Granade 2018 *(in preparation)* .</span></span>
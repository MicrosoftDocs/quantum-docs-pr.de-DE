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
# <a name="randomwalkphaseestimation-operation"></a>Randomwalkphaseschätzungsvorgang

Namespace: [Microsoft. Quantum. Research. Charakterisierung](xref:Microsoft.Quantum.Research.Characterization)

Paketen [](https://nuget.org/packages/)


Führt eine iterative Phasen Schätzung mithilfe eines zufälligen Durchlaufs aus, um einen ungefähren bayesschen Rückschluss auf die klassischen Messergebnisse eines bestimmten Oracle-und eigen Zustands festzustellen.

```qsharp
operation RandomWalkPhaseEstimation (initialMean : Double, initialStdDev : Double, nMeasurements : Int, maxMeasurements : Int, unwind : Int, oracle : Microsoft.Quantum.Oracles.ContinuousOracle, targetState : Qubit[]) : Double
```


## <a name="input"></a>Eingabe

### <a name="initialmean--double"></a>initialmean: [Double](xref:microsoft.quantum.lang-ref.double)

Mittelwert der anfänglichen normalen Vorverteilung über $ \phi $.


### <a name="initialstddev--double"></a>initialstddev: [Double](xref:microsoft.quantum.lang-ref.double)

Standard Abweichung der anfänglichen normalen früheren Verteilung über $ \phi $.


### <a name="nmeasurements--int"></a>nmessungen: [int](xref:microsoft.quantum.lang-ref.int)

Anzahl der Messungen, die in der abschließenden nach-unten-Schätzung akzeptiert werden sollen.


### <a name="maxmeasurements--int"></a>maxmessungen: [int](xref:microsoft.quantum.lang-ref.int)

Die Gesamtanzahl der Messungen, die durchgeführt werden können, bevor der Vorgang als fehlgeschlagen eingestuft wird.


### <a name="unwind--int"></a>entladen: [int](xref:microsoft.quantum.lang-ref.int)

Anzahl der zu debuggende Ergebnisse, wenn Konsistenzprüfungen fehlschlagen.


### <a name="oracle--continuousoracle"></a>Oracle: [continuousoracle](xref:Microsoft.Quantum.Oracles.ContinuousOracle)

Ein Vorgang, der eine einheitliche $U $ darstellt, sodass $U (t) \ket{\phi} = e ^ {i t \phi}\ket{\phi} $ für Eigen Zustände $ \ket{\phi} $ mit unbekannter Phase $ \phi \ in \mathbb{r} ^ + $.


### <a name="targetstate--qubit"></a>targetState: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Ein Register, für das $U $ agiert.



## <a name="output--double"></a>Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)

Die letzte Schätzung $ \hat{\phi} \mathrel{: =} \expect [\phi] $, bei der die Annahme über dem Posterior mit allen akzeptierten Daten liegt.

## <a name="remarks"></a>Hinweise

### <a name="iterative-phase-estimation-and-eigenstates"></a>Iterative Phasen Schätzung und eigen Zustände

Im Allgemeinen muss das Eingabe Register `eigenstate` nicht den eigen Zustand $ \ket{\phi} $ von $U $ aufweisen, kann jedoch eine übergeordnete Position gegenüber eigen Zuständen sein. Angenommen, der Eingabe Zustand wird von \begin{align} \ket{\psi} & = \sum \_ {j} \alpha \_ j \ket{\phi \_ j} angegeben. \end{align}, wobei "$ \{ \alpha \_ j $" \} komplexe Koeffizienten wie "$ \sum \_ j | \alpha \_ j | ^ 2 = $1" und "where $U \ket{\phi \_ j} = \phi \_ j\ket {\ Phi \_ j} $" sind.

Anschließend wird die iterative Phasen Schätzung letztendlich in einen einzelnen eigen Zustand konvergiert, wie im [Entwicklungs Handbuch](xref:microsoft.quantum.libraries.characterization#iterative-phase-estimation-without-eigenstates)beschrieben.

### <a name="experiment-design"></a>Experiment Entwurf

Die Messzeiten $t $ und der inversionswinkel $ \an die an über gegebene Daten `oracle` werden gemäß der *Partikel Annahme Heuristik* , \begin{align} \Der Ta \sim \pr (\phi), \quad t \ca \frac {1} {\variance{\phi}}.
\end{align} diese Heuristik eignet sich optimal, um die erwartete nachträgliche Abweichung in der iterativen Phasen Schätzung unter der Annahme eines normalen vorherigen zu verringern.

### <a name="optimality"></a>Mindestgrößeneinheit

Dieser Vorgang entspricht der optimalen Schätzung für die Phase $ \phi $, die mithilfe des quadratischen Verlusts $L (\phi, \hat{\phi}) \mathrel{: =} (\phi-\hat{\phi}) ^ 2 $ ausgewertet wird.

Weitere Informationen zu den Statistiken der iterativen Phasen Schätzung finden Sie unter [bayyesian-Phasen Schätzung](xref:microsoft.quantum.libraries.characterization#bayesian-phase-estimation) .

## <a name="references"></a>Referenzen

- Ferrie *et al.* 2011 [doi: 10/TFX](https://doi.org/10.1007/s11128-012-0407-6), [arXiv: 1110.3067](https://arxiv.org/abs/1110.3067).
- Wiebe *et al.* 2013 [doi: 10/TF3](https://doi.org/10.1103/PhysRevLett.112.190501), [arXiv: 1309.0876](https://arxiv.org/abs/1309.0876)
- Wiebe und Granade 2018 *(in Vorbereitung)* .
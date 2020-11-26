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
# <a name="robustphaseestimation-operation"></a>RobustPhaseEstimation-Vorgang

Namespace: [Microsoft. Quantum. Charakterisierung](xref:Microsoft.Quantum.Characterization)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Führt den robusten, nicht iterativen Quantum-Phasen-Schätz Algorithmus für ein bestimmtes Oracle `U` und einen eigen Zustand aus und bietet eine einzelne, in Echtzeit angegebene Schätzung der Phase mit Varianz Skalierung am Heisenberg-Limit.

```qsharp
operation RobustPhaseEstimation (bitsPrecision : Int, oracle : Microsoft.Quantum.Oracles.DiscreteOracle, targetState : Qubit[]) : Double
```


## <a name="input"></a>Eingabe

### <a name="bitsprecision--int"></a>bitationcision: [int](xref:microsoft.quantum.lang-ref.int)

Dies bietet eine Schätzung von $ \phi $ mit der Standardabweichung $ \sigma \le 2 \ Pi/2 ^ \text{bitspcision} $, wobei eine Reihe von Abfragen skaliert wird, wie z. b. $ \sigma \le 10,7 \pi/\text{# of queries} $.


### <a name="oracle--discreteoracle"></a>Oracle: [diskreteoracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)

Ein Vorgang, der $U ^ m $ für angegebene ganzzahlige $m $ implementiert.


### <a name="targetstate--qubit"></a>targetState: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Ein Quantum-Register, für das $U $ agiert. Wenn ein eigen Status $ \ket{\phi} $ von $U $ gespeichert wird, $U \ket{\phi} = e ^ {i\phi} \ket{\phi} $ für $ \phi\in (-\pi, \pi] $ eine unbekannte Phase.



## <a name="output--double"></a>Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)



## <a name="remarks"></a>Bemerkungen

Der Grenzwert für eine große Anzahl von Abfragen Cramer-Rao unteren Grenzen der geschätzten Schätzung von $ \phi $ entspricht $ \sigma \ge 2 \pi/\text{# of queries} $.

## <a name="references"></a>Referenzen

- Robuste Kalibrierung eines universellen Single-Qubit Gate-Set über die robuste Phasen Schätzung Shelby Kimmel, Guang Hao Low, Theodore J. Yoder https://arxiv.org/abs/1502.02677
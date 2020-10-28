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
# <a name="robustphaseestimation-operation"></a>RobustPhaseEstimation-Vorgang

Namespace: [Microsoft. Quantum. Charakterisierung](xref:Microsoft.Quantum.Characterization)

Paketen [](https://nuget.org/packages/)


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



## <a name="remarks"></a>Hinweise

Der Grenzwert für eine große Anzahl von Abfragen Cramer-Rao unteren Grenzen der geschätzten Schätzung von $ \phi $ entspricht $ \sigma \ge 2 \pi/\text{# of queries} $.

## <a name="references"></a>Referenzen

- Robuste Kalibrierung eines universellen Single-Qubit Gate-Set über die robuste Phasen Schätzung Shelby Kimmel, Guang Hao Low, Theodore J. Yoder https://arxiv.org/abs/1502.02677
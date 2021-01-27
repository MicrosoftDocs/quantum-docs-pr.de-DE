---
uid: Microsoft.Quantum.Characterization.DiscretePhaseEstimationIteration
title: Diskretephaseschätzungsiterations-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: DiscretePhaseEstimationIteration
qsharp.summary: Performs a single iteration of an iterative (classically-controlled) phase estimation algorithm using integer powers of a unitary oracle.
ms.openlocfilehash: 03e2300dcc2d2cb42992e074833c8cd2530e898b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839973"
---
# <a name="discretephaseestimationiteration-operation"></a>Diskretephaseschätzungsiterations-Vorgang

Namespace: [Microsoft. Quantum. Charakterisierung](xref:Microsoft.Quantum.Characterization)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Führt eine einzelne Iteration eines iterativen (klassisch gesteuerten) Phasen Schätz Algorithmus mithilfe von ganzzahligen Kräften eines einheitlichen Oracle aus.

```qsharp
operation DiscretePhaseEstimationIteration (oracle : Microsoft.Quantum.Oracles.DiscreteOracle, power : Int, theta : Double, targetState : Qubit[], controlQubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>Eingabe

### <a name="oracle--discreteoracle"></a>Oracle: [diskreteoracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)

Der Vorgang, der für eine ganze Zahl und ein Register ausgeführt wird, sodass $U ^ m $ auf das angegebene Register angewendet wird, wobei $U $ die einheitliche ist, deren Phase geschätzt werden soll, und wobei $m $ die ganzzahlige Potenz ist, die dem Oracle zugewiesen ist.


### <a name="power--int"></a>Power: [int](xref:microsoft.quantum.lang-ref.int)

Gibt an, wie oft das angegebene einheitliche Oracle angewendet werden soll.


### <a name="theta--double"></a>-Ta: [Double](xref:microsoft.quantum.lang-ref.double)

Der Winkel, um den die Phase auf dem Qubit des-Steuer Elements vor dem Ausführen des Ziel Zustands invertieren soll.


### <a name="targetstate--qubit"></a>targetState: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Das Registrierungsstatus, auf das der angegebene einheitliche Oracle reagiert hat.


### <a name="controlqubit--qubit"></a>controlqubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Ein zusätzliches Qubit, das verwendet wird, um die Anwendung des angegebenen Oracle zu steuern.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)


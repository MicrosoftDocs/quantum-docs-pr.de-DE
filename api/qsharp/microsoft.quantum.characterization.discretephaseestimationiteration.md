---
uid: Microsoft.Quantum.Characterization.DiscretePhaseEstimationIteration
title: Diskretephaseschätzungsiterations-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: DiscretePhaseEstimationIteration
qsharp.summary: Performs a single iteration of an iterative (classically-controlled) phase estimation algorithm using integer powers of a unitary oracle.
ms.openlocfilehash: 167b53d7108c64d11a4f258d17e90ba78d7dd8d8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703655"
---
# <a name="discretephaseestimationiteration-operation"></a>Diskretephaseschätzungsiterations-Vorgang

Namespace: [Microsoft. Quantum. Charakterisierung](xref:Microsoft.Quantum.Characterization)

Paketen [](https://nuget.org/packages/)


Führt eine einzelne Iteration eines iterativen (klassisch gesteuerten) Phasen Schätz Algorithmus mithilfe von ganzzahligen Kräften eines einheitlichen Oracle aus.

```qsharp
operation DiscretePhaseEstimationIteration (oracle : Microsoft.Quantum.Oracles.DiscreteOracle, power : Int, theta : Double, targetState : Qubit[], controlQubit : Qubit) : Unit
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


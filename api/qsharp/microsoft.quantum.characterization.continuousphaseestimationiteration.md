---
uid: Microsoft.Quantum.Characterization.ContinuousPhaseEstimationIteration
title: Continuousphaseschätzationiteration-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: ContinuousPhaseEstimationIteration
qsharp.summary: Performs a single iteration of an iterative (classically-controlled) phase estimation algorithm using arbitrary real powers of a unitary oracle.
ms.openlocfilehash: 925b9040f6d9cda074b18a6f9079ccb653f9fa98
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851906"
---
# <a name="continuousphaseestimationiteration-operation"></a>Continuousphaseschätzationiteration-Vorgang

Namespace: [Microsoft. Quantum. Charakterisierung](xref:Microsoft.Quantum.Characterization)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Führt eine einzelne Iteration eines iterativen (klassisch kontrollierten) Phasen Schätz Algorithmus mit beliebigen echten Kräften eines einheitlichen Oracle aus.

```qsharp
operation ContinuousPhaseEstimationIteration (oracle : Microsoft.Quantum.Oracles.ContinuousOracle, time : Double, theta : Double, targetState : Qubit[], controlQubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>Eingabe

### <a name="oracle--continuousoracle"></a>Oracle: [continuousoracle](xref:Microsoft.Quantum.Oracles.ContinuousOracle)

Ein Vorgang, der auf einem Double-$t $ und einem Register ausgeführt wird, sodass $U ^ t $ auf das angegebene Register angewendet wird, wobei $U $ die einheitliche ist, deren Phase geschätzt werden soll, und wobei $t $ die ganzzahlige Potenz ist, die dem Oracle zugewiesen ist.


### <a name="time--double"></a>Zeit: [Double](xref:microsoft.quantum.lang-ref.double)

Gibt an, wie oft das angegebene einheitliche Oracle angewendet werden soll.


### <a name="theta--double"></a>-Ta: [Double](xref:microsoft.quantum.lang-ref.double)

Der Winkel, um den die Phase auf dem Qubit des-Steuer Elements vor dem Ausführen des Ziel Zustands invertieren soll.


### <a name="targetstate--qubit"></a>targetState: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Das Registrierungsstatus, auf das der angegebene einheitliche Oracle reagiert hat.


### <a name="controlqubit--qubit"></a>controlqubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)





## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)


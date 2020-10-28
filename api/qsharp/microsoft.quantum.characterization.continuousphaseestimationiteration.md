---
uid: Microsoft.Quantum.Characterization.ContinuousPhaseEstimationIteration
title: Continuousphaseschätzationiteration-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: ContinuousPhaseEstimationIteration
qsharp.summary: Performs a single iteration of an iterative (classically-controlled) phase estimation algorithm using arbitrary real powers of a unitary oracle.
ms.openlocfilehash: a3914a4b19e3b898b6de8808699da09d386f487a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703656"
---
# <a name="continuousphaseestimationiteration-operation"></a>Continuousphaseschätzationiteration-Vorgang

Namespace: [Microsoft. Quantum. Charakterisierung](xref:Microsoft.Quantum.Characterization)

Paketen [](https://nuget.org/packages/)


Führt eine einzelne Iteration eines iterativen (klassisch kontrollierten) Phasen Schätz Algorithmus mit beliebigen echten Kräften eines einheitlichen Oracle aus.

```qsharp
operation ContinuousPhaseEstimationIteration (oracle : Microsoft.Quantum.Oracles.ContinuousOracle, time : Double, theta : Double, targetState : Qubit[], controlQubit : Qubit) : Unit
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


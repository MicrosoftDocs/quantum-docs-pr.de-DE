---
uid: Microsoft.Quantum.Simulation.TimeDependentTrotterSimulationAlgorithmImpl
title: Timedependenttrottersimulationalgorithmimpl-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TimeDependentTrotterSimulationAlgorithmImpl
qsharp.summary: Implementation of multiple Trotter steps to approximate a unitary operator that solves the time-dependent Schrödinger equation.
ms.openlocfilehash: f4f8a9265dc25305819da5ae1002f02b7efd1952
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203449"
---
# <a name="timedependenttrottersimulationalgorithmimpl-operation"></a>Timedependenttrottersimulationalgorithmimpl-Vorgang

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Implementierung mehrerer trockschritte zur Annäherung an einen einheitlichen Operator, der die zeitabhängige Schrödinger-Gleichung löst.

```qsharp
operation TimeDependentTrotterSimulationAlgorithmImpl (trotterStepSize : Double, trotterOrder : Int, maxTime : Double, evolutionSchedule : Microsoft.Quantum.Simulation.EvolutionSchedule, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Eingabe

### <a name="trotterstepsize--double"></a>trotterstepsize: [Double](xref:microsoft.quantum.lang-ref.double)

Dauer der simulierten Zeitentwicklung in einem einzelnen trockschritt.


### <a name="trotterorder--int"></a>trotterorder: [int](xref:microsoft.quantum.lang-ref.int)

Reihenfolge des trockintegrator. Dies muss entweder 1 oder eine gerade Zahl sein.


### <a name="maxtime--double"></a>maxTime: [Double](xref:microsoft.quantum.lang-ref.double)

Gesamtdauer der Simulation $t $.


### <a name="evolutionschedule--evolutionschedule"></a>evolutionschedule: [evolutionschedule](xref:Microsoft.Quantum.Simulation.EvolutionSchedule)

Eine umfassende Beschreibung des zeitabhängigen Systems, das simuliert werden soll.


### <a name="qubits--qubit"></a>Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Die von der Simulation abgewickelten Qubits.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)


---
uid: Microsoft.Quantum.Simulation.TrotterSimulationAlgorithmImpl
title: Trottersimulationalgorithmimpl-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TrotterSimulationAlgorithmImpl
qsharp.summary: Makes repeated calls to `TrotterStep` to approximate the time-evolution operator exp(_-iHt_).
ms.openlocfilehash: 5b796245e2a4434228260a229cb61be66f3e38d6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203398"
---
# <a name="trottersimulationalgorithmimpl-operation"></a>Trottersimulationalgorithmimpl-Vorgang

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Führt wiederkehrende Aufrufe von aus `TrotterStep` , um den Zeit-Evolution-Operator Exp (_-IHT_) zu nähern.

```qsharp
operation TrotterSimulationAlgorithmImpl (trotterStepSize : Double, trotterOrder : Int, maxTime : Double, evolutionGenerator : Microsoft.Quantum.Simulation.EvolutionGenerator, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Eingabe

### <a name="trotterstepsize--double"></a>trotterstepsize: [Double](xref:microsoft.quantum.lang-ref.double)

Dauer der simulierten Zeitentwicklung in einem einzelnen trockschritt.


### <a name="trotterorder--int"></a>trotterorder: [int](xref:microsoft.quantum.lang-ref.int)

Reihenfolge des trockintegrator. Dies muss entweder 1 oder eine gerade Zahl sein.


### <a name="maxtime--double"></a>maxTime: [Double](xref:microsoft.quantum.lang-ref.double)

Gesamtdauer der Simulation $t $.


### <a name="evolutiongenerator--evolutiongenerator"></a>evolutiongenerator: [evolutiongenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)

Eine umfassende Beschreibung des Systems, das simuliert werden soll.


### <a name="qubits--qubit"></a>Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Die von der Simulation abgewickelten Qubits.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)


---
uid: Microsoft.Quantum.Simulation.TrotterStepImpl
title: Trotterstepimpl-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TrotterStepImpl
qsharp.summary: Implements time-evolution by a term contained in a `GeneratorSystem`.
ms.openlocfilehash: bc6c3c6656da319fce9c7c48824dbc4ad75ccc83
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203414"
---
# <a name="trotterstepimpl-operation"></a>Trotterstepimpl-Vorgang

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Implementiert die Zeitentwicklung mit einem in einem enthaltenen Begriff `GeneratorSystem` .

```qsharp
operation TrotterStepImpl (evolutionGenerator : Microsoft.Quantum.Simulation.EvolutionGenerator, idx : Int, stepsize : Double, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Eingabe

### <a name="evolutiongenerator--evolutiongenerator"></a>evolutiongenerator: [evolutiongenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)

Eine umfassende Beschreibung des Systems, das simuliert werden soll.


### <a name="idx--int"></a>idx: [int](xref:microsoft.quantum.lang-ref.int)

Ganzzahliger Index zu einem Begriff im beschriebenen System.


### <a name="stepsize--double"></a>stepSize: [Double](xref:microsoft.quantum.lang-ref.double)

Multiplikator für die Dauer der Zeit-Evolution nach Begriff, indiziert von `idx` .


### <a name="qubits--qubit"></a>Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Die von der Simulation abgewickelten Qubits.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)


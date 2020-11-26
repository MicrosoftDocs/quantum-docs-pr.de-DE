---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE._prepareTrialStateWrapper
title: _prepareTrialStateWrapper Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: _prepareTrialStateWrapper
qsharp.summary: Private wrapper around PrepareTrialState to make it compatible with EstimateFrequencyA by defining an adjoint. EstimateFrequencyA has built-in emulation feature when targeting the QuantumSimulator, which speeds up its execution.
ms.openlocfilehash: 8e1a39cbd307a467ab7f0466c90722e1c8c46d4a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224682"
---
# <a name="_preparetrialstatewrapper-operation"></a>_prepareTrialStateWrapper Vorgang

Namespace: [Microsoft. Quantum. Chemistry. jordanwigner. vqe](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)

Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Privater Wrapper um preparezstate, um ihn mit estimatefrequescya kompatibel zu machen, indem ein Adjoint-Wert definiert wird.
Estimatefrequencya verfügt über eine integrierte Emulations Funktion, wenn der quantumsimulator als Ziel verwendet wird, wodurch die Ausführung beschleunigt wird.

```qsharp
operation _prepareTrialStateWrapper (inputState : (Int, Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState[]), qubits : Qubit[]) : Unit is Adj
```


## <a name="input"></a>Eingabe

### <a name="inputstate--intjordanwignerinputstate"></a>inputstate: ([int](xref:microsoft.quantum.lang-ref.int),[jordanwignerinputstate](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState)[])

Die Jordan-Wigner Eingabe, die für die Durchführung von preparezalstate erforderlich ist.


### <a name="qubits--qubit"></a>Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Ein Qubit-Register.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)


---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE._prepareTrialStateWrapper
title: _prepareTrialStateWrapper Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: _prepareTrialStateWrapper
qsharp.summary: Private wrapper around PrepareTrialState to make it compatible with EstimateFrequencyA by defining an adjoint. EstimateFrequencyA has built-in emulation feature when targeting the QuantumSimulator, which speeds up its execution.
ms.openlocfilehash: bfd7b9ce8e8b2c8f322d676c640f8c2488655516
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703092"
---
# <a name="_preparetrialstatewrapper-operation"></a>_prepareTrialStateWrapper Vorgang

Namespace: [Microsoft. Quantum. Chemistry. jordanwigner. vqe](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)

Paketen [](https://nuget.org/packages/)


Privater Wrapper um preparezstate, um ihn mit estimatefrequescya kompatibel zu machen, indem ein Adjoint-Wert definiert wird.
Estimatefrequencya verfügt über eine integrierte Emulations Funktion, wenn der quantumsimulator als Ziel verwendet wird, wodurch die Ausführung beschleunigt wird.

```qsharp
operation _prepareTrialStateWrapper (inputState : (Int, Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState[]), qubits : Qubit[]) : Unit
```


## <a name="input"></a>Eingabe

### <a name="inputstate--intjordanwignerinputstate"></a>inputstate: ([int](xref:microsoft.quantum.lang-ref.int),[jordanwignerinputstate](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState)[])

Die Jordan-Wigner Eingabe, die für die Durchführung von preparezalstate erforderlich ist.


### <a name="qubits--qubit"></a>Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Ein Qubit-Register.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)


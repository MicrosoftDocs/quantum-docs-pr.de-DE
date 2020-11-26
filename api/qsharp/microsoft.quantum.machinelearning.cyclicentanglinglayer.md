---
uid: Microsoft.Quantum.MachineLearning.CyclicEntanglingLayer
title: Zyklicentanglinglayer-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: CyclicEntanglingLayer
qsharp.summary: Returns an array of singly controlled rotations along a given axis, arranged cyclically across a register of qubits, and parameterized by distinct model parameters.
ms.openlocfilehash: 5421765e36ef3e8e744e118206dafcb2bb582cc2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211932"
---
# <a name="cyclicentanglinglayer-function"></a>Zyklicentanglinglayer-Funktion

Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)

Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Gibt ein Array von einzeln kontrollierten Drehungen entlang einer angegebenen Achse zurück, das zyklisch über ein Register von Qubits angeordnet und durch unterschiedliche Modellparameter parametrisiert wird.

```qsharp
function CyclicEntanglingLayer (nQubits : Int, axis : Pauli, stride : Int) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a>Eingabe

### <a name="nqubits--int"></a>nqubits: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der Qubits, die durch die angegebene Ebene bearbeitet wurden.


### <a name="axis--pauli"></a>Achse: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

Die Drehungs Achse für jede Drehung in der angegebenen Ebene.


### <a name="stride--int"></a>Stride: [int](xref:microsoft.quantum.lang-ref.int)

Die Trennung zwischen den Ziel-und Steuerelement Indizes für jede Drehung.



## <a name="output--controlledrotation"></a>Ausgabe: [controlledrotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]

Ein Array von zwei-Qubit-gesteuerten Rotationen, das zyklisch über ein Register von `nQubits` Qubits angelegt ist.
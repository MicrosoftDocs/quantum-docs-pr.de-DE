---
uid: Microsoft.Quantum.MachineLearning.LocalRotationsLayer
title: Localrotationslayer-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: LocalRotationsLayer
qsharp.summary: Returns an array of uncontrolled (single-qubit) rotations along a given axis, with one rotation for each qubit in a register, parameterized by distinct model parameters.
ms.openlocfilehash: 1549f24427f19bacbadf72e00c1c0181b64bcb73
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211728"
---
# <a name="localrotationslayer-function"></a>Localrotationslayer-Funktion

Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)

Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Gibt ein Array von unkontrollierten Rotationen (Single-Qubit) entlang einer angegebenen Achse zurück, wobei für jedes Qubit in einem Register eine Drehung durch unterschiedliche Modellparameter parametrisiert ist.

```qsharp
function LocalRotationsLayer (nQubits : Int, axis : Pauli) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a>Eingabe

### <a name="nqubits--int"></a>nqubits: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der Qubits, die durch die angegebene Ebene bearbeitet wurden.


### <a name="axis--pauli"></a>Achse: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

Die Drehungs Achse für jede Drehung in der angegebenen Ebene.



## <a name="output--controlledrotation"></a>Ausgabe: [controlledrotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]

Ein Array von kontrollierten Rotationen für die angegebene Achse, eines auf jedem der `nQubits` Qubits.
---
uid: Microsoft.Quantum.MachineLearning.PartialRotationsLayer
title: Partialrotationslayer-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: PartialRotationsLayer
qsharp.summary: Returns an array of single-qubit rotations along a given axis, parameterized by distinct model parameters.
ms.openlocfilehash: ab964d2c43a13a5daf64aefdeccd1c26cd371ff4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722430"
---
# <a name="partialrotationslayer-function"></a>Partialrotationslayer-Funktion

Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)

Paketen [](https://nuget.org/packages/)


Gibt ein Array von Single-Qubit-Drehungen entlang einer angegebenen Achse zurück, die durch unterschiedliche Modellparameter parametrisiert werden.

```qsharp
function PartialRotationsLayer (idxsQubits : Int[], axis : Pauli) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a>Eingabe

### <a name="idxsqubits--int"></a>idxsqubits: [int](xref:microsoft.quantum.lang-ref.int)[]

Indizes für die Qubits, die als Ziele für jede Drehung verwendet werden sollen.


### <a name="axis--pauli"></a>Achse: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

Die Drehungs Achse für jede Drehung in der angegebenen Ebene.



## <a name="output--controlledrotation"></a>Ausgabe: [controlledrotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]

Ein Array von kontrollierten Rotationen für die angegebene Achse, eines auf jedem der `nQubits` Qubits.
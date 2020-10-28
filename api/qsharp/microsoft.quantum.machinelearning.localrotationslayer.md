---
uid: Microsoft.Quantum.MachineLearning.LocalRotationsLayer
title: Localrotationslayer-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: LocalRotationsLayer
qsharp.summary: Returns an array of uncontrolled (single-qubit) rotations along a given axis, with one rotation for each qubit in a register, parameterized by distinct model parameters.
ms.openlocfilehash: 8a3557f76d5d7a7b6375e5640cf6d11172cd38a6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723466"
---
# <a name="localrotationslayer-function"></a>Localrotationslayer-Funktion

Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)

Paketen [](https://nuget.org/packages/)


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
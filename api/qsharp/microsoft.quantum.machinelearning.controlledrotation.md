---
uid: Microsoft.Quantum.MachineLearning.ControlledRotation
title: Benutzerdefinierter controlledrotation-Typ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ControlledRotation
qsharp.summary: Describes a controlled rotation in terms of its target and control indices, rotation axis, and index into a model parameter vector.
ms.openlocfilehash: 231afe65da3640218cbc97b9d49eae21bf6e1786
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847391"
---
# <a name="controlledrotation-user-defined-type"></a>Benutzerdefinierter controlledrotation-Typ

Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)

Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Beschreibt eine gesteuerte Drehung in Bezug auf die Ziel-und Steuerelement Indizes, die Drehungs Achse und den Index in einen Modellparameter Vektor.

```qsharp

newtype ControlledRotation = ((TargetIndex : Int, ControlIndices : Int[]), Axis : Pauli, ParameterIndex : Int);
```



## <a name="named-items"></a>Benannte Elemente

### <a name="targetindex--int"></a>TargetIndex: [int](xref:microsoft.quantum.lang-ref.int)

Index des zielqubits für diese gesteuerte Drehung.
### <a name="controlindices--int"></a>Controlindices: [int](xref:microsoft.quantum.lang-ref.int)[]

Ein Array der-Steuerelement-Qubit-Indizes für diese Drehung.
### <a name="axis--pauli"></a>Achse: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

Die Achse für diese Drehung.
### <a name="parameterindex--int"></a>Parameterindex: [int](xref:microsoft.quantum.lang-ref.int)

Ein Index in einem Modellparameter Vektor, der den Winkel für diese Drehung beschreibt.

## <a name="example"></a>Beispiel

Folgendes stellt eine Drehung zum $X $-Achse des ersten Qubit in einem Register dar, gesteuert auf das zweite Qubit und mit einem Winkel, der durch den vierten Parameter in einem sequenziellen Modell angegeben wird:

```qsharp
let controlledRotation = ControlledRotation(
    (0, [1]),
    PauliX,
    3
)
```

## <a name="remarks"></a>Bemerkungen

Eine unkontrollierte Drehung kann dargestellt werden, indem `ControlIndices` auf ein leeres Array von Indizes festgelegt wird `new Int[0]` .
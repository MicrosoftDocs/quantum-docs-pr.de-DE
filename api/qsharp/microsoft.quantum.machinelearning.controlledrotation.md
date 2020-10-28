---
uid: Microsoft.Quantum.MachineLearning.ControlledRotation
title: Benutzerdefinierter controlledrotation-Typ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ControlledRotation
qsharp.summary: Describes a controlled rotation in terms of its target and control indices, rotation axis, and index into a model parameter vector.
ms.openlocfilehash: afc425c16ab550fd414e656484c9ff6f0f8f3ef4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702065"
---
# <a name="controlledrotation-user-defined-type"></a>Benutzerdefinierter controlledrotation-Typ

Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)

Paketen [](https://nuget.org/packages/)


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

## <a name="remarks"></a>Hinweise

Eine unkontrollierte Drehung kann dargestellt werden, indem `ControlIndices` auf ein leeres Array von Indizes festgelegt wird `new Int[0]` .
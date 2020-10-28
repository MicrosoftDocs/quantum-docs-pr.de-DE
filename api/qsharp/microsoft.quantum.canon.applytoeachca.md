---
uid: Microsoft.Quantum.Canon.ApplyToEachCA
title: Applydeeachca-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachCA
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `CA` indicates that the single-qubit operation is controllable and adjointable.
ms.openlocfilehash: b24fbb8c7a1a55c0a7750c5d096a61f4824dadfb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704959"
---
# <a name="applytoeachca-operation"></a>Applydeeachca-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Wendet für jedes Element in einem Register einen Single-Qubit-Vorgang an.
Der-Modifizierer `CA` gibt an, dass der Single-Qubit-Vorgang steuerbar und adjointable ist.

```qsharp
operation ApplyToEachCA<'T> (singleElementOperation : ('T => Unit is Adj + Ctl), register : 'T[]) : Unit
```


## <a name="input"></a>Eingabe

### <a name="singleelementoperation--t--unit-adj--ctl"></a>singleelementoperation: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL

Der auf die einzelnen Qubits anzuwendende Vorgang.


### <a name="register--t"></a>Register: 't []

Ein Array von Qubits, auf das der angegebene Vorgang angewendet werden soll.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Das Ziel, für das der Vorgang fungiert.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. applyyeach](xref:Microsoft.Quantum.Canon.ApplyToEach)
---
uid: Microsoft.Quantum.Canon.ApplyToEachIndexA
title: Applydeeachindexa-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachIndexA
qsharp.summary: Applies a single-qubit operation to each indexed element in a register. The modifier `A` indicates that the single-qubit operation is adjointable.
ms.openlocfilehash: 0fe0697e6f1d9441c2d2ad2c7396f6da8daa0e1e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704951"
---
# <a name="applytoeachindexa-operation"></a>Applydeeachindexa-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Wendet einen Single-Qubit-Vorgang auf jedes indizierte Element in einem Register an.
Der-Modifizierer `A` gibt an, dass der Single-Qubit-Vorgang adjointable ist.

```qsharp
operation ApplyToEachIndexA<'T> (singleElementOperation : ((Int, 'T) => Unit is Adj), register : 'T[]) : Unit
```


## <a name="input"></a>Eingabe

### <a name="singleelementoperation--intt--unit-adj"></a>singleelementoperation: ([int](xref:microsoft.quantum.lang-ref.int), t) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ

Der auf die einzelnen Qubits anzuwendende Vorgang.


### <a name="register--t"></a>Register: 't []

Ein Array von Qubits, auf das der angegebene Vorgang angewendet werden soll.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Das Ziel, für das jeder der Vorgänge fungiert.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. applyteachindex](xref:Microsoft.Quantum.Canon.ApplyToEachIndex)
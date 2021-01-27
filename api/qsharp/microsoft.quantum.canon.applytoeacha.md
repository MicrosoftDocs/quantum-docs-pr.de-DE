---
uid: Microsoft.Quantum.Canon.ApplyToEachA
title: Applydeeacha-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachA
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `A` indicates that the single-qubit operation is adjointable.
ms.openlocfilehash: da901db2bb3c70186bfe0c8812b5710198d1dff3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844617"
---
# <a name="applytoeacha-operation"></a>Applydeeacha-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Wendet für jedes Element in einem Register einen Single-Qubit-Vorgang an.
Der-Modifizierer `A` gibt an, dass der Single-Qubit-Vorgang adjointable ist.

```qsharp
operation ApplyToEachA<'T> (singleElementOperation : ('T => Unit is Adj), register : 'T[]) : Unit is Adj
```


## <a name="input"></a>Eingabe

### <a name="singleelementoperation--t--unit--is-adj"></a>singleelementoperation: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ

Der auf die einzelnen Qubits anzuwendende Vorgang.


### <a name="register--t"></a>Register: 't []

Ein Array von Qubits, auf das der angegebene Vorgang angewendet werden soll.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Das Ziel, für das der Vorgang fungiert.

## <a name="example"></a>Beispiel

Bereiten Sie einen "3-Qubit $ \ket{+} $"-Status vor:

```qsharp
using (register = Qubit[3]) {
    ApplyToEach(H, register);
}
```

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. applyyeach](xref:Microsoft.Quantum.Canon.ApplyToEach)
---
uid: Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsA
title: Applydefirstthreequbitsa-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstThreeQubitsA
qsharp.summary: Applies an operation to the first three qubits in the register. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: c3374ceba9f442f9315d4b5fc54b158327124926
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208770"
---
# <a name="applytofirstthreequbitsa-operation"></a>Applydefirstthreequbitsa-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Wendet einen Vorgang auf die ersten drei Qubits im Register an.
Der-Modifizierer `A` gibt an, dass der Vorgang adjointable ist.

```qsharp
operation ApplyToFirstThreeQubitsA (op : ((Qubit, Qubit, Qubit) => Unit is Adj), register : Qubit[]) : Unit is Adj
```


## <a name="input"></a>Eingabe

### <a name="op--qubitqubitqubit--unit--is-adj"></a>OP: ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ

Ein Vorgang, der auf die ersten drei Qubits angewendet werden soll.


### <a name="register--qubit"></a>Register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Qubit-Array mit den ersten drei Qubits, auf die der Vorgang angewendet wird.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Bemerkungen

Das entspricht:

```qsharp
op(register[0], register[1], register[2]);
```

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. applyyfirstthreequbits](xref:Microsoft.Quantum.Canon.ApplyToFirstThreeQubits)
---
uid: Microsoft.Quantum.Canon.ApplyPauliFromBitString
title: Applypaulifrombitstring-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyPauliFromBitString
qsharp.summary: Applies a Pauli operator on each qubit in an array if the corresponding bit of a Boolean array matches a given input.
ms.openlocfilehash: cf4c99ec5134fac788cdd4c8a057258790152a82
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209059"
---
# <a name="applypaulifrombitstring-operation"></a>Applypaulifrombitstring-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Wendet einen Pauli-Operator auf jedes Qubit in einem Array an, wenn das entsprechende Bit eines booleschen Arrays mit einer angegebenen Eingabe übereinstimmt.

```qsharp
operation ApplyPauliFromBitString (pauli : Pauli, bitApply : Bool, bits : Bool[], qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Eingabe

### <a name="pauli--pauli"></a>Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

Der Pauli-Operator, auf den angewendet wird. `qubits[idx]``bitsApply == bits[idx]`


### <a name="bitapply--bool"></a>bitapply: [bool](xref:microsoft.quantum.lang-ref.bool)

Anwenden von Pauli, wenn Bit dieser Wert ist


### <a name="bits--bool"></a>Bits: [bool](xref:microsoft.quantum.lang-ref.bool)[]

Boolesches Register, das angibt, welches entsprechende Qubit in `qubits` operiert werden soll


### <a name="qubits--qubit"></a>Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Das Quantum-Register, für das der angegebene Pauli-Operator selektiv angewendet wird.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Bemerkungen

Das boolesche Array und das Quantum-Register müssen die gleiche Länge aufweisen.
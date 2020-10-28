---
uid: Microsoft.Quantum.Canon.ApplyPauliFromBitString
title: Applypaulifrombitstring-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyPauliFromBitString
qsharp.summary: Applies a Pauli operator on each qubit in an array if the corresponding bit of a Boolean array matches a given input.
ms.openlocfilehash: 09754accb92c1339b781003e5722e3c8f5884e6f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705106"
---
# <a name="applypaulifrombitstring-operation"></a>Applypaulifrombitstring-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Wendet einen Pauli-Operator auf jedes Qubit in einem Array an, wenn das entsprechende Bit eines booleschen Arrays mit einer angegebenen Eingabe übereinstimmt.

```qsharp
operation ApplyPauliFromBitString (pauli : Pauli, bitApply : Bool, bits : Bool[], qubits : Qubit[]) : Unit
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



## <a name="remarks"></a>Hinweise

Das boolesche Array und das Quantum-Register müssen die gleiche Länge aufweisen.
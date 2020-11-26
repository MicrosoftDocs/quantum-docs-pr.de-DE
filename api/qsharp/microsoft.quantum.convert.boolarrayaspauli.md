---
uid: Microsoft.Quantum.Convert.BoolArrayAsPauli
title: Boolarrayaspauli-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: BoolArrayAsPauli
qsharp.summary: Given a bit string, returns a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators.
ms.openlocfilehash: 8e7088ec3918165d7b2afb1056a8319c6fb17796
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96214278"
---
# <a name="boolarrayaspauli-function"></a>Boolarrayaspauli-Funktion

Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt bei Angabe einer Bitzeichenfolge einen multiqubit-Pauli-Operator zurück, der als Array von Single-Qubit-Pauli-Operatoren dargestellt wird.

```qsharp
function BoolArrayAsPauli (pauli : Pauli, bitApply : Bool, bits : Bool[]) : Pauli[]
```


## <a name="input"></a>Eingabe

### <a name="pauli--pauli"></a>Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

Der Pauli-Operator, der auf Qubits angewendet wird, wobei `bitsApply == bits[idx]` .


### <a name="bitapply--bool"></a>bitapply: [bool](xref:microsoft.quantum.lang-ref.bool)

Anwenden von Pauli, wenn Bit dieser Wert ist.


### <a name="bits--bool"></a>Bits: [bool](xref:microsoft.quantum.lang-ref.bool)[]

Boolesches Array.



## <a name="output--pauli"></a>Ausgabe: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]



## <a name="remarks"></a>Bemerkungen

Das boolesche Array und das Quantum-Register müssen die gleiche Länge aufweisen.
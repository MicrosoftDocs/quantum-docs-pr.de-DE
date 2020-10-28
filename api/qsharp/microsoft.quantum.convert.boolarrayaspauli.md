---
uid: Microsoft.Quantum.Convert.BoolArrayAsPauli
title: Boolarrayaspauli-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: BoolArrayAsPauli
qsharp.summary: Given a bit string, returns a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators.
ms.openlocfilehash: c5ef71322dae248fc2c6b1db3adf891de7d72488
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703025"
---
# <a name="boolarrayaspauli-function"></a>Boolarrayaspauli-Funktion

Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)

Paketen [](https://nuget.org/packages/)


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



## <a name="remarks"></a>Hinweise

Das boolesche Array und das Quantum-Register müssen die gleiche Länge aufweisen.
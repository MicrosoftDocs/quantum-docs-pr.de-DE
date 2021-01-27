---
uid: Microsoft.Quantum.Convert.BoolArrayAsPauli
title: Boolarrayaspauli-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: BoolArrayAsPauli
qsharp.summary: Given a bit string, returns a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators.
ms.openlocfilehash: c11ca05ad8a939d704547c65a8e8a6537d0df4b7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98834246"
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
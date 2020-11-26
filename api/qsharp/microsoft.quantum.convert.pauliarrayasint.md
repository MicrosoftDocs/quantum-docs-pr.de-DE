---
uid: Microsoft.Quantum.Convert.PauliArrayAsInt
title: Pauliarrayasint-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: PauliArrayAsInt
qsharp.summary: Encodes a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators into an integer.
ms.openlocfilehash: 6077110cc07c8626b22eb404c1de096ed43efcc3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224240"
---
# <a name="pauliarrayasint-function"></a>Pauliarrayasint-Funktion

Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Codiert einen multiqubit-Pauli-Operator, der als Array von Single-Qubit-Pauli-Operatoren dargestellt wird, in eine ganze Zahl.

```qsharp
function PauliArrayAsInt (paulis : Pauli[]) : Int
```


## <a name="input"></a>Eingabe

### <a name="paulis--pauli"></a>Paulis: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]

Ein Array mit höchstens 31 Single-Qubit-Pauli-Operatoren.



## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)

Eine Ganzzahl, die eindeutig identifiziert `paulis` , wie unten beschrieben.

## <a name="remarks"></a>Bemerkungen

Jeder Pauli-Operator kann mit zwei Bits codiert werden: $ $ \begin{align} \boldone \mapsto 00, \quad X \mapsto 01, \quad Y \mapsto 11, \quad Z \mapsto 10.
\end{align} $ $

Bei einem Array von Pauli-Operatoren `[P0, ..., Pn]` gibt diese Funktion eine ganze Zahl mit binärer Erweiterung zurück, die durch Verkettung der Zuordnungen der einzelnen Pauli-Operatoren in Big-Endian-Reihenfolge gebildet wird `bits(Pn) ... bits(P0)` .
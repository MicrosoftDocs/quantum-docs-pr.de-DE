---
uid: Microsoft.Quantum.Convert.PauliArrayAsInt
title: Pauliarrayasint-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: PauliArrayAsInt
qsharp.summary: Encodes a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators into an integer.
ms.openlocfilehash: f8ec468dd0f0cfd0d868dfc79ff715b3b4fc2f4a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702924"
---
# <a name="pauliarrayasint-function"></a>Pauliarrayasint-Funktion

Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)

Paketen [](https://nuget.org/packages/)


Codiert einen multiqubit-Pauli-Operator, der als Array von Single-Qubit-Pauli-Operatoren dargestellt wird, in eine ganze Zahl.

```qsharp
function PauliArrayAsInt (paulis : Pauli[]) : Int
```


## <a name="input"></a>Eingabe

### <a name="paulis--pauli"></a>Paulis: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]

Ein Array mit höchstens 31 Single-Qubit-Pauli-Operatoren.



## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)

Eine Ganzzahl, die eindeutig identifiziert `paulis` , wie unten beschrieben.

## <a name="remarks"></a>Hinweise

Jeder Pauli-Operator kann mit zwei Bits codiert werden: $ $ \begin{align} \boldone \mapsto 00, \quad X \mapsto 01, \quad Y \mapsto 11, \quad Z \mapsto 10.
\end{align} $ $

Bei einem Array von Pauli-Operatoren `[P0, ..., Pn]` gibt diese Funktion eine ganze Zahl mit binärer Erweiterung zurück, die durch Verkettung der Zuordnungen der einzelnen Pauli-Operatoren in Big-Endian-Reihenfolge gebildet wird `bits(Pn) ... bits(P0)` .
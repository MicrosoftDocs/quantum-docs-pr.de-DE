---
uid: Microsoft.Quantum.Diagnostics._flipToBasis
title: _flipToBasis Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: _flipToBasis
qsharp.summary: >-
  Applies unitaries that map $\ket{0}\otimes\cdots\ket{0}$ to $\ket{\psi_0} \otimes \ket{\psi_{n - 1}}$, where $\ket{\psi_k}$ depends on `basis[k]`.

  The correspondence between value of `basis[k]` and $\ket{\psi_k}$ is the following:

  - `basis[k]=0` $\rightarrow \ket{0}$. - `basis[k]=1` $\rightarrow \ket{1}$. - `basis[k]=2` $\rightarrow \ket{+}$. - `basis[k]=3` $\rightarrow \ket{i}$ ( +1 eigenstate of Pauli Y ).
ms.openlocfilehash: d46c42846066befafda2af22f7b6e861cb260c33
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98831004"
---
# <a name="_fliptobasis-operation"></a>_flipToBasis Vorgang

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Wendet die unimaps an, die $ \ket {0} \otimes\cdoz\ket {0} $ zu $ \ket{\ psi_0} \otimes \ket{\ psi_ {n-1}} $ zuordnen, wobei $ \ket{\ psi_k} $ von abhängt `basis[k]` .

Die Entsprechung zwischen Wert `basis[k]` und $ \ket{\ psi_k} $ lautet wie folgt:

- `basis[k]=0` $ \rightarrow \ket {0} $.
- `basis[k]=1` $ \rightarrow \ket {1} $.
- `basis[k]=2` $ \rightarrow \ket{+} $.
- `basis[k]=3` $ \rightarrow \ket{i} $ (+ 1 eigen Status von Pauli Y).

```qsharp
operation _flipToBasis (basis : Int[], qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Eingabe

### <a name="basis--int"></a>Basis: [int](xref:microsoft.quantum.lang-ref.int)[]

Array von Single-Qubit-Basis-IDs (0 <= ID <= 3), eine für jedes Element von Qubits.


### <a name="qubits--qubit"></a>Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Das zu verwendende Qubit.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)


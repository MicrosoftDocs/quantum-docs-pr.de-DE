---
uid: Microsoft.Quantum.Intrinsic.ExpFrac
title: Expfrac-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: ExpFrac
qsharp.summary: >-
  Applies the exponential of a multi-qubit Pauli operator with an argument given by a dyadic fraction.

  \begin{align} e^{i \pi k [P_0 \otimes P_1 \cdots P_{N-1}] / 2^n}, \end{align} where $P_i$ is the $i$th element of `paulis`, and where $N = $`Length(paulis)`.
ms.openlocfilehash: 8ccea068dd61aaf8c1ba384969adef5644e8401e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198994"
---
# <a name="expfrac-operation"></a>Expfrac-Vorgang

Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Wendet den Exponentialwert eines multiqubit-Pauli-Operators mit einem Argument an, das von einem dyadic-Bruchteil angegeben wird.

\begin{align} e ^ {i \pi k [P_0 \otimes P_1 \cdots P_ {N-1}]/2 ^ N}, \end{align}, wobei $P _I $ das $i $ th-Element von `paulis` und WHERE $N = $ ist `Length(paulis)` .

```qsharp
operation ExpFrac (paulis : Pauli[], numerator : Int, power : Int, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Eingabe

### <a name="paulis--pauli"></a>Paulis: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]

Array von Single-Qubit-Pauli-Werten, die die tensorflow-Produkt Faktoren für jedes Qubit angeben.


### <a name="numerator--int"></a>Zähler: [int](xref:microsoft.quantum.lang-ref.int)

Der Zähler ($k $) in der dyadic-Bruch Darstellung des Winkels, um den das Qubit-Register gedreht werden soll.


### <a name="power--int"></a>Power: [int](xref:microsoft.quantum.lang-ref.int)

Potenz von zwei ($n $), die den Nenner des Winkels angibt, um den das Qubit-Register gedreht werden soll.


### <a name="qubits--qubit"></a>Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Registrieren Sie sich, um die angegebene Drehung auf anzuwenden.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)


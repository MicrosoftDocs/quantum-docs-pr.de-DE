---
uid: Microsoft.Quantum.Intrinsic.Measure
title: Measure-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Measure
qsharp.summary: >-
  Performs a joint measurement of one or more qubits in the specified Pauli bases.

  The output result is given by the distribution: \begin{align} \Pr(\texttt{Zero} | \ket{\psi}) = \frac12 \braket{ \psi \mid| \left( \boldone + P_0 \otimes P_1 \otimes \cdots \otimes P_{N-1} \right) \mid| \psi }, \end{align} where $P_i$ is the $i$th element of `bases`, and where $N = \texttt{Length}(\texttt{bases})$. That is, measurement returns a `Result` $d$ such that the eigenvalue of the observed measurement effect is $(-1)^d$.
ms.openlocfilehash: bf0a606b1bfc8c4762245422450ec26907ec1946
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98818770"
---
# <a name="measure-operation"></a>Measure-Vorgang

Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Führt eine gemeinsame Messung von einem oder mehreren Qubits in den angegebenen Pauli-Basen aus.

Das Ausgabe Ergebnis wird durch die Verteilung angegeben: \begin{align} \pr (\texttt{Zero} | \ket{\psi}) = \bruch12 \braket{\psi \mid | \left (\boldone + P_0 \otimes P_1 \otimes \cdots \otimes P_ {N-1} \right) \mid | \psi}, \end{align}, wobei $P _I $ das $i $ th-Element von ist. `bases` und WHERE $N = \texttt{verlän} (\texttt{Bases}) $.
Das heißt, die Messung gibt eine `Result` $d $ zurück, sodass der Eigen Wert des beobachteten Mess Effekts $ (-1) ^ d $ ist.

```qsharp
operation Measure (bases : Pauli[], qubits : Qubit[]) : Result
```


## <a name="input"></a>Eingabe

### <a name="bases--pauli"></a>Basen: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]

Array von Single-Qubit-Pauli-Werten, die die tensorflow-Produkt Faktoren für jedes Qubit angeben.


### <a name="qubits--qubit"></a>Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Das Register der zu messenden Qubits.



## <a name="output--__invalidresult__"></a>Ausgabe: __ungültig <Result>__

`Zero` , wenn der Eigen Wert $ + $1 festgestellt wird, und, `One` Wenn der Eigen Wert $-$1 festgestellt wird.

## <a name="remarks"></a>Bemerkungen

Wenn die Längen Array-und Qubit-Arrays unterschiedlich lang sind, schlägt der Vorgang fehl.
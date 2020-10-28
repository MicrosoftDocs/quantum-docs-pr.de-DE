---
uid: Microsoft.Quantum.Intrinsic.Measure
title: Measure-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Measure
qsharp.summary: >-
  Performs a joint measurement of one or more qubits in the specified Pauli bases.

  The output result is given by the distribution: \begin{align} \Pr(\texttt{Zero} | \ket{\psi}) = \frac12 \braket{ \psi \mid| \left( \boldone + P_0 \otimes P_1 \otimes \cdots \otimes P_{N-1} \right) \mid| \psi }, \end{align} where $P_i$ is the $i$th element of `bases`, and where $N = \texttt{Length}(\texttt{bases})$. That is, measurement returns a `Result` $d$ such that the eigenvalue of the observed measurement effect is $(-1)^d$.
ms.openlocfilehash: 56ddfbe5e63692e477ad75bde6b1b16269ed20c0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702102"
---
# <a name="measure-operation"></a>Measure-Vorgang

Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)

Paketen [](https://nuget.org/packages/)


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

## <a name="remarks"></a>Hinweise

Wenn die Längen Array-und Qubit-Arrays unterschiedlich lang sind, schlägt der Vorgang fehl.
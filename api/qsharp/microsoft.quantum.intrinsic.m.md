---
uid: Microsoft.Quantum.Intrinsic.M
title: M-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: M
qsharp.summary: >-
  Performs a measurement of a single qubit in the Pauli $Z$ basis.

  The output result is given by the distribution \begin{align} \Pr(\texttt{Zero} | \ket{\psi}) = \braket{\psi | 0} \braket{0 | \psi}. \end{align}
ms.openlocfilehash: 8d4b120385bfc7086a7cb0e3f77034c760d78d92
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707154"
---
# <a name="m-operation"></a>M-Vorgang

Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)

Paketen [](https://nuget.org/packages/)


Führt eine Messung eines einzelnen Qubit in der Pauli-$Z $ aus.

Das Ausgabe Ergebnis wird durch die Distribution \begin{align} \pr (\texttt{Zero} | \ket{\psi}) = \braket{\psi | 0} \braket{0 | \psi}.
\end{align}

```qsharp
operation M (qubit : Qubit) : Result
```


## <a name="input"></a>Eingabe

### <a name="qubit--qubit"></a>Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Qubit, das gemessen werden soll.



## <a name="output--__invalidresult__"></a>Ausgabe: __ungültig <Result>__

`Zero` , wenn der Eigen Wert $ + $1 festgestellt wird, und, `One` Wenn der Eigen Wert $-$1 festgestellt wird.

## <a name="remarks"></a>Hinweise

Äquivalent zu:

```qsharp
Measure([PauliZ], [qubit]);
```
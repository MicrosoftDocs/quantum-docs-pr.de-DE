---
uid: Microsoft.Quantum.Chemistry.JordanWigner.SelectZ
title: Selectz-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: SelectZ
qsharp.summary: A unitary $U$ that applies the Pauli $Z$ gate on a qubits $p$ conditioned on an index state $\ket{p}$. That is, $$ \begin{align} U\ket{p}\ket{\psi} = \ket{p}Z\_p\ket{\psi} \end{align} $$
ms.openlocfilehash: 08abe3f465432bf98f35090c59fb4d952c3b4882
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224716"
---
# <a name="selectz-operation"></a>Selectz-Vorgang

Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Ein einheitlicher $U $, der die Pauli $Z $ Gate auf eine Qubits $p $ anwendet, die auf einem Index Status $ \ket{p} $ bedingt ist. Das heißt: $ $ \begin{align} u\ket {p} \ Ket {\ PSI} = \ket{p}Z \_ p\ket {\ PSI} \end{align} $ $

```qsharp
operation SelectZ (indexRegister : Microsoft.Quantum.Arithmetic.LittleEndian, targetRegister : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Eingabe

### <a name="indexregister--littleendian"></a>Indexregister: [littleerdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Der Status $ \ket{p} $ dieses Registers bestimmt das Qubit, auf dem $Z $ angewendet wird.


### <a name="targetregister--qubit"></a>targetregiester: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Das Register der Qubits, auf die die Pauli-Operatoren angewendet werden.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)


---
uid: Microsoft.Quantum.Canon.ApplyFermionicSWAP
title: Applyfermionicswap-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyFermionicSWAP
qsharp.summary: Applies the Fermionic SWAP.
ms.openlocfilehash: 0c470705843a6360df0a72374570d86571397e41
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218800"
---
# <a name="applyfermionicswap-operation"></a>Applyfermionicswap-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Wendet den fermionic-Swap an.

```qsharp
operation ApplyFermionicSWAP (qubit1 : Qubit, qubit2 : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a>BESCHREIBUNG

Dies vertauscht die Qubits im Wesentlichen beim Anwenden einer globalen Phase von-1, wenn beide Qubits 1 s sind. Behält die antisymmetrisierung von orbitalen bei.
Weitere Informationen finden Sie unter .

Dieser Vorgang wird durch den einheitlichen Operator \begin{align} F_ {Swap} \mathrel{: =} \begin{bmatrix} 1 & 0 & 0 & 0 \\ \\ 0 & 0 & 1 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 &-1 \\ \\ \end{bmatrix}.
\end{align}

## <a name="input"></a>Eingabe

### <a name="qubit1--qubit"></a>qubit1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Das erste Qubit, das ausgetauscht werden soll.


### <a name="qubit2--qubit"></a>qubit2: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Das zweite Qubit, das ausgetauscht werden soll.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>Referenzen

- [*Ryan babbush, Nathan Wiebe, Jarrod McClean, James McClain, Hartmut netven, Garnet Kin-Lic Chan*, arXiv: 1706.00023](https://arxiv.org/pdf/1706.00023.pdf)

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. intrinsisch. Swap](xref:Microsoft.Quantum.Intrinsic.SWAP)
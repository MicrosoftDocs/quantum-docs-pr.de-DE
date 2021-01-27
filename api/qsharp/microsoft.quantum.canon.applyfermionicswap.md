---
uid: Microsoft.Quantum.Canon.ApplyFermionicSWAP
title: Applyfermionicswap-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyFermionicSWAP
qsharp.summary: Applies the Fermionic SWAP.
ms.openlocfilehash: 334f407a32dabc8f4e0a1a29c8f06a1b9f40dc59
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845055"
---
# <a name="applyfermionicswap-operation"></a>Applyfermionicswap-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Wendet den fermionic-Swap an.

```qsharp
operation ApplyFermionicSWAP (qubit1 : Qubit, qubit2 : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a>Beschreibung

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



## <a name="references"></a>References

- [*Ryan babbush, Nathan Wiebe, Jarrod McClean, James McClain, Hartmut netven, Garnet Kin-Lic Chan*, arXiv: 1706.00023](https://arxiv.org/pdf/1706.00023.pdf)

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. intrinsisch. Swap](xref:Microsoft.Quantum.Intrinsic.SWAP)
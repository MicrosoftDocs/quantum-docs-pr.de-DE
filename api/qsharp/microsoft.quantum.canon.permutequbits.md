---
uid: Microsoft.Quantum.Canon.PermuteQubits
title: Permutequbits-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: PermuteQubits
qsharp.summary: Permutes qubits by using the SWAP operation.
ms.openlocfilehash: 2fbbe0d99ad1383d77cb08ff6b03bcebd8a1971f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852325"
---
# <a name="permutequbits-operation"></a>Permutequbits-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Permutes Qubits mithilfe des Swap-Vorgangs.

```qsharp
operation PermuteQubits (ordering : Int[], register : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Eingabe

### <a name="ordering--int"></a>Reihenfolge: [int](xref:microsoft.quantum.lang-ref.int)[]

Beschreibt die neue Reihenfolge der Qubits, bei der das Qubit bei Index i nun die Reihenfolge [i] hat.


### <a name="register--qubit"></a>Register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Das Qubit-Register, das bearbeitet werden soll.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="example"></a>Beispiel

Bei Angabe von Order = [2, 1, 0] und Register $ \ket{\ alpha_0} \ket{\ alpha_1} \ket{\ alpha_2} $ ändert permutequbits das Register in $ \ket{\ alpha_2} \ket{\ alpha_1} \ket{\ alpha_0} $.

```qsharp
// The following two lines are equivalent
PermuteQubits([2, 1, 0], register);
SWAP(register[0], register[2]);
```
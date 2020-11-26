---
uid: Microsoft.Quantum.Canon.ApplyCNOTChainWithTarget
title: Applycnotchainwithtarget-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCNOTChainWithTarget
qsharp.summary: Computes the parity of an array of qubits into a target qubit.
ms.openlocfilehash: 8ec85ce5805b3bbd1e1f7c739f27de3a861bc79e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219106"
---
# <a name="applycnotchainwithtarget-operation"></a>Applycnotchainwithtarget-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Berechnet die Parität eines Arrays von Qubits in einem Ziel-Qubit.

```qsharp
operation ApplyCNOTChainWithTarget (qubits : Qubit[], targetQubit : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a>BESCHREIBUNG

Wenn sich das Array anfänglich im Status $ \ket{q_0} \ket{q_1} \cdots \ket{Q_ {\text{Target}}} $ befindet, wird der endgültige Zustand durch $ \ket{q_0} \ket{q_1 \oplus q_0} \cdots \ket{Q_ {n-1} \oplus \cdots \oplus q_0 \oplus Q_ {\text{target}}} $ angegeben.

## <a name="input"></a>Eingabe

### <a name="qubits--qubit"></a>Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Array von Qubits, für das die Parität berechnet wird.


### <a name="targetqubit--qubit"></a>targetqubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Endgültiges Qubit, in das die Parität von ' Qubits ' XoReD ist.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Bemerkungen

Die folgenden sind gleichwertig:

```qsharp
ApplyCNOTChainWithTarget(Most(qs), Last(qs));
```

and

```qsharp
ApplyCNOTChain(qs);
```
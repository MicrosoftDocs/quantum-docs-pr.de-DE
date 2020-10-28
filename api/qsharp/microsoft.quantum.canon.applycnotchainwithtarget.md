---
uid: Microsoft.Quantum.Canon.ApplyCNOTChainWithTarget
title: Applycnotchainwithtarget-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCNOTChainWithTarget
qsharp.summary: Computes the parity of an array of qubits into a target qubit.
ms.openlocfilehash: fd0a0f3e1db89946aec2c63f3cde7a021608eea5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705439"
---
# <a name="applycnotchainwithtarget-operation"></a>Applycnotchainwithtarget-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Berechnet die Parität eines Arrays von Qubits in einem Ziel-Qubit.

```qsharp
operation ApplyCNOTChainWithTarget (qubits : Qubit[], targetQubit : Qubit) : Unit
```


## <a name="description"></a>BESCHREIBUNG

Wenn sich das Array anfänglich im Status $ \ket{q_0} \ket{q_1} \cdots \ket{Q_ {\text{Target}}} $ befindet, wird der endgültige Zustand durch $ \ket{q_0} \ket{q_1 \oplus q_0} \cdots \ket{Q_ {n-1} \oplus \cdots \oplus q_0 \oplus Q_ {\text{target}}} $ angegeben.

## <a name="input"></a>Eingabe

### <a name="qubits--qubit"></a>Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Array von Qubits, für das die Parität berechnet wird.


### <a name="targetqubit--qubit"></a>targetqubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Endgültiges Qubit, in das die Parität von ' Qubits ' XoReD ist.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Hinweise

Die folgenden sind gleichwertig:

```qsharp
ApplyCNOTChainWithTarget(Most(qs), Last(qs));
```

und

```qsharp
ApplyCNOTChain(qs);
```
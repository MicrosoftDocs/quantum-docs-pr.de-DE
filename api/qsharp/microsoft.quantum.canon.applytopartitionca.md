---
uid: Microsoft.Quantum.Canon.ApplyToPartitionCA
title: Applytopartitionca-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToPartitionCA
qsharp.summary: Applies a pair of operations to a given partition of a register into two parts. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: b33670a91af5cbf280fdda0e57ddbbf8c9013e91
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208301"
---
# <a name="applytopartitionca-operation"></a>Applytopartitionca-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Wendet ein paar von Vorgängen auf eine bestimmte Partition eines Registers in zwei Teilen an.
Der-Modifizierer `CA` gibt an, dass der Vorgang steuerbar und adjointable ist.

```qsharp
operation ApplyToPartitionCA (op : ((Qubit[], Qubit[]) => Unit is Ctl + Adj), numberOfQubitsToFirstArgument : Int, target : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Eingabe

### <a name="op--qubitqubit--unit--is-adj--ctl"></a>OP: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL

Das auf die angegebene Partition anzuwendende paar von Vorgängen.


### <a name="numberofqubitstofirstargument--int"></a>numofqubitstofirstargument: [int](xref:microsoft.quantum.lang-ref.int)

Anzahl der Qubits aus dem Ziel, die in den ersten Teil der Partition eingefügt werden sollen.
Die restlichen Qubits bilden den zweiten Teil der Partition.


### <a name="target--qubit"></a>Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Ein Register von Qubits, die durch den angegebenen zwei Vorgang partitioniert und verarbeitet werden.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. applytopartition](xref:Microsoft.Quantum.Canon.ApplyToPartition)
---
uid: Microsoft.Quantum.Canon.ApplyToPartitionA
title: Applytopartitiona-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToPartitionA
qsharp.summary: Applies a pair of operations to a given partition of a register into two parts. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: f8f773e9fc3c18467185f9717a235649be8b385a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841303"
---
# <a name="applytopartitiona-operation"></a>Applytopartitiona-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Wendet ein paar von Vorgängen auf eine bestimmte Partition eines Registers in zwei Teilen an.
Der-Modifizierer `A` gibt an, dass der Vorgang adjointable ist.

```qsharp
operation ApplyToPartitionA (op : ((Qubit[], Qubit[]) => Unit is Adj), numberOfQubitsToFirstArgument : Int, target : Qubit[]) : Unit is Adj
```


## <a name="input"></a>Eingabe

### <a name="op--qubitqubit--unit--is-adj"></a>OP: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ

Das auf die angegebene Partition anzuwendende paar von Vorgängen.


### <a name="numberofqubitstofirstargument--int"></a>numofqubitstofirstargument: [int](xref:microsoft.quantum.lang-ref.int)

Anzahl der Qubits aus dem Ziel, die in den ersten Teil der Partition eingefügt werden sollen.
Die restlichen Qubits bilden den zweiten Teil der Partition.


### <a name="target--qubit"></a>Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Ein Register von Qubits, die durch den angegebenen zwei Vorgang partitioniert und verarbeitet werden.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. applytopartition](xref:Microsoft.Quantum.Canon.ApplyToPartition)
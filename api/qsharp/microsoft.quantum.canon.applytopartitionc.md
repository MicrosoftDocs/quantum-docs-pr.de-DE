---
uid: Microsoft.Quantum.Canon.ApplyToPartitionC
title: Applytopartitionc-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToPartitionC
qsharp.summary: Applies a pair of operations to a given partition of a register into two parts. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: 840c93c653d71af1a82fb0dc51d9e056176ba88b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704711"
---
# <a name="applytopartitionc-operation"></a>Applytopartitionc-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Wendet ein paar von Vorgängen auf eine bestimmte Partition eines Registers in zwei Teilen an.
Der-Modifizierer `C` gibt an, dass der Vorgang steuerbar ist.

```qsharp
operation ApplyToPartitionC (op : ((Qubit[], Qubit[]) => Unit is Ctl), numberOfQubitsToFirstArgument : Int, target : Qubit[]) : Unit
```


## <a name="input"></a>Eingabe

### <a name="op--qubitqubit--unit-ctl"></a>OP: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL

Das auf die angegebene Partition anzuwendende paar von Vorgängen.


### <a name="numberofqubitstofirstargument--int"></a>numofqubitstofirstargument: [int](xref:microsoft.quantum.lang-ref.int)

Anzahl der Qubits aus dem Ziel, die in den ersten Teil der Partition eingefügt werden sollen.
Die restlichen Qubits bilden den zweiten Teil der Partition.


### <a name="target--qubit"></a>Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Ein Register von Qubits, die durch den angegebenen zwei Vorgang partitioniert und verarbeitet werden.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. applytopartition](xref:Microsoft.Quantum.Canon.ApplyToPartition)
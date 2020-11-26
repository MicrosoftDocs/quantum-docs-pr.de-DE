---
uid: Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver
title: Applyoprepeatedlyover-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyOpRepeatedlyOver
qsharp.summary: Applies the same op over a qubit register multiple times.
ms.openlocfilehash: 343392d5a6af07cdc45fd8bab6656d59a6f2b350
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218307"
---
# <a name="applyoprepeatedlyover-operation"></a>Applyoprepeatedlyover-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Wendet denselben op-Vorgang über ein Qubit-Register mehrmals an.

```qsharp
operation ApplyOpRepeatedlyOver (op : (Qubit[] => Unit), targets : Int[][], register : Qubit[]) : Unit
```


## <a name="input"></a>Eingabe

### <a name="op--qubit--unit"></a>OP: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit) 

Ein Vorgang, der mehrmals auf das Qubit-Register angewendet werden soll.


### <a name="targets--int"></a>Ziele: [int](xref:microsoft.quantum.lang-ref.int)[] []

Geschmestete Arrays, die die Ziele des OP beschreiben. Jedes Array muss eine Liste von int enthalten, die die zu verwendenden Qubits beschreibt.


### <a name="register--qubit"></a>Register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Das Qubit-Register, das bearbeitet werden soll.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. applyseriesofops](xref:Microsoft.Quantum.Canon.ApplySeriesOfOps)
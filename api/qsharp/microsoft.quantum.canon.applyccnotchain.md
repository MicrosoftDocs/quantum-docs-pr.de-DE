---
uid: Microsoft.Quantum.Canon.ApplyCCNOTChain
title: Applyccnotchain-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCCNOTChain
qsharp.summary: Implements a cascade of CCNOT gates controlled on corresponding bits of two qubit registers, acting on the next qubit of one of the registers. Starting from the qubits at position 0 in both registers as controls, CCNOT is applied to the qubit at position 1 of the target register, then controlled by the qubits at position 1 acting on the qubit at position 2 in the target register, etc., ending with an action on the target qubit in position `Length(nQubits)-1`.
ms.openlocfilehash: 275f31ea636d15eb0d78e5148e8af6b58d22729d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209654"
---
# <a name="applyccnotchain-operation"></a>Applyccnotchain-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Implementiert eine Cascade von ccnot Gates, die für die entsprechenden Bits zweier Qubit-Register gesteuert werden, und verhält sich für das nächste Qubit eines der Register.
Beginnend mit den Qubits an Position 0 in beiden Registern als Steuerelemente, wird ccnot auf das Qubit an Position 1 des Ziel Registers angewendet und dann von den Qubits an Position 1 gesteuert, die auf dem Qubit an Position 2 im Zielregister agiert, usw., und endet mit einer Aktion auf dem Ziel-Qubit an der Position `Length(nQubits)-1` .

```qsharp
operation ApplyCCNOTChain (register : Qubit[], targets : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Eingabe

### <a name="register--qubit"></a>Register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Das Qubit-Register wird nur für Steuerelemente verwendet.


### <a name="targets--qubit"></a>Ziele: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Ein Qubit-Register, das für Steuerelemente und als Ziel verwendet wird.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Bemerkungen

Für das Ziel-Qubit-Register muss ein Qubit mehr als das andere Register vorhanden sein.
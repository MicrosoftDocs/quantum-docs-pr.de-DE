---
uid: Microsoft.Quantum.Canon.ApplyCCNOTChain
title: Applyccnotchain-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCCNOTChain
qsharp.summary: Implements a cascade of CCNOT gates controlled on corresponding bits of two qubit registers, acting on the next qubit of one of the registers. Starting from the qubits at position 0 in both registers as controls, CCNOT is applied to the qubit at position 1 of the target register, then controlled by the qubits at position 1 acting on the qubit at position 2 in the target register, etc., ending with an action on the target qubit in position `Length(nQubits)-1`.
ms.openlocfilehash: e4f38e9bb54839076b817f6e61e96ca6a550576b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705455"
---
# <a name="applyccnotchain-operation"></a>Applyccnotchain-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Implementiert eine Cascade von ccnot Gates, die für die entsprechenden Bits zweier Qubit-Register gesteuert werden, und verhält sich für das nächste Qubit eines der Register.
Beginnend mit den Qubits an Position 0 in beiden Registern als Steuerelemente, wird ccnot auf das Qubit an Position 1 des Ziel Registers angewendet und dann von den Qubits an Position 1 gesteuert, die auf dem Qubit an Position 2 im Zielregister agiert, usw., und endet mit einer Aktion auf dem Ziel-Qubit an der Position `Length(nQubits)-1` .

```qsharp
operation ApplyCCNOTChain (register : Qubit[], targets : Qubit[]) : Unit
```


## <a name="input"></a>Eingabe

### <a name="register--qubit"></a>Register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Das Qubit-Register wird nur für Steuerelemente verwendet.


### <a name="targets--qubit"></a>Ziele: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Ein Qubit-Register, das für Steuerelemente und als Ziel verwendet wird.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Hinweise

Für das Ziel-Qubit-Register muss ein Qubit mehr als das andere Register vorhanden sein.
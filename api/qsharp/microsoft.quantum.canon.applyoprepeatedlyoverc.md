---
uid: Microsoft.Quantum.Canon.ApplyOpRepeatedlyOverC
title: Applyoprepeatedlyoverc-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyOpRepeatedlyOverC
qsharp.summary: Applies the same op over a qubit register multiple times.
ms.openlocfilehash: effd61e6c012dcf81a83383c3fd43cf745d18117
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705119"
---
# <a name="applyoprepeatedlyoverc-operation"></a>Applyoprepeatedlyoverc-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Wendet denselben op-Vorgang über ein Qubit-Register mehrmals an.

```qsharp
operation ApplyOpRepeatedlyOverC (op : (Qubit[] => Unit is Ctl), targets : Int[][], register : Qubit[]) : Unit
```


## <a name="input"></a>Eingabe

### <a name="op--qubit--unit-ctl"></a>OP: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL

Ein Vorgang, der mehrmals auf das Qubit-Register angewendet werden soll.


### <a name="targets--int"></a>Ziele: [int](xref:microsoft.quantum.lang-ref.int)[] []

Geschmestete Arrays, die die Ziele des OP beschreiben. Jedes Array muss eine Liste von int enthalten, die die zu verwendenden Qubits beschreibt.


### <a name="register--qubit"></a>Register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Das Qubit-Register, das bearbeitet werden soll.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. applyseriesofops](xref:Microsoft.Quantum.Canon.ApplySeriesOfOps)
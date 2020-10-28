---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOpsCA
title: Applyseriesofopsca-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOpsCA
qsharp.summary: Applies a list of ops and their targets sequentially on an array. (Adjoint + Controlled)
ms.openlocfilehash: 2327a693e528cf46f95eae5ee052e9dd9b6ee187
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705007"
---
# <a name="applyseriesofopsca-operation"></a>Applyseriesofopsca-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Wendet eine Liste von OPS und deren Zielen sequenziell auf ein Array an. (Adjoint + gesteuert)

```qsharp
operation ApplySeriesOfOpsCA<'T> (listOfOps : ('T[] => Unit is Adj + Ctl)[], targets : Int[][], register : 'T[]) : Unit
```


## <a name="input"></a>Eingabe

### <a name="listofops--t--unit-adj--ctl"></a>listOf: 't [] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL []

Die Liste der OPS, die jeweils ein nicht-Array enthalten, das angewendet werden soll. Sie werden sequenziell, der niedrigste Index zuerst angewendet.
Jede muss sowohl über einen Adjoint-als auch überwachten Funktor verfügen.


### <a name="targets--int"></a>Ziele: [int](xref:microsoft.quantum.lang-ref.int)[] []

Geschmestete Arrays, die die Ziele des OP beschreiben. Jedes Array muss eine Liste von Punkten enthalten, in denen die zu verwendenden Indizes beschrieben werden.


### <a name="register--t"></a>Register: 't []

Das Qubit-Register, das bearbeitet werden soll.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF



## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. applyoprepeatedlyover](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)
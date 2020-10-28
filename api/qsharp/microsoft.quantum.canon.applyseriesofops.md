---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOps
title: Applyseriesofops-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOps
qsharp.summary: Applies a list of ops and their targets sequentially on an array.
ms.openlocfilehash: aff0bcb831960153166e88aef1f05e000125d5d8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705026"
---
# <a name="applyseriesofops-operation"></a>Applyseriesofops-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Wendet eine Liste von OPS und deren Zielen sequenziell auf ein Array an.

```qsharp
operation ApplySeriesOfOps<'T> (listOfOps : ('T[] => Unit)[], targets : Int[][], register : 'T[]) : Unit
```


## <a name="input"></a>Eingabe

### <a name="listofops--t--unit-"></a>listOf: 't [] => [Unit](xref:microsoft.quantum.lang-ref.unit) []

Die Liste der OPS, die jeweils ein nicht-Array enthalten, das angewendet werden soll. Sie werden sequenziell, der niedrigste Index zuerst angewendet.


### <a name="targets--int"></a>Ziele: [int](xref:microsoft.quantum.lang-ref.int)[] []

Geschmestete Arrays, die die Ziele des OP beschreiben. Jedes Array muss eine Liste von Punkten enthalten, in denen die zu verwendenden Indizes beschrieben werden.


### <a name="register--t"></a>Register: 't []

Das Qubit-Register, das bearbeitet werden soll.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF



## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. applyoprepeatedlyover](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)
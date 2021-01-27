---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOps
title: Applyseriesofops-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOps
qsharp.summary: Applies a list of ops and their targets sequentially on an array.
ms.openlocfilehash: b086b01b0be86bd25a6d6cdef26bfbb53e484cb2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841496"
---
# <a name="applyseriesofops-operation"></a>Applyseriesofops-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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



## <a name="example"></a>Beispiel

Folgendes gilt für Exp ([Paulix, pauliy], 0,5) für Qubits 0, 1//dann X bis Qubit 2 Let OPS = [Exp ([Paulix, pauliy], 0,5, _), applyjefirstqubit (X, _)]; Let-Indizes = [[0, 1], [2]]; Applyseriesofops (OPS, Indizes, qubitarray);

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. applyoprepeatedlyover](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)
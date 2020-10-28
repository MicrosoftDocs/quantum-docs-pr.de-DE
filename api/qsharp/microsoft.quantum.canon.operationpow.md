---
uid: Microsoft.Quantum.Canon.OperationPow
title: Operationpow-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: OperationPow
qsharp.summary: >-
  Raises an operation to a power.

  That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.
ms.openlocfilehash: 5cf9017175f44a8a0b8f865624a6c312d25aded1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703955"
---
# <a name="operationpow-function"></a>Operationpow-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Löst einen Vorgang für eine Stromversorgung aus.

Das heißt, wenn ein Vorgang, der ein Gate $U $ darstellt, einen neuen Vorgang $U ^ m $ für eine Power $m $ zurückgibt.

```qsharp
function OperationPow<'T> (op : ('T => Unit), power : Int) : ('T => Unit)
```


## <a name="input"></a>Eingabe

### <a name="op--t--unit"></a>OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) 

Ein Vorgang $U $, der das Gate darstellt, das wiederholt werden soll.


### <a name="power--int"></a>Power: [int](xref:microsoft.quantum.lang-ref.int)

Gibt an, wie oft $U $ wiederholt werden soll.



## <a name="output--t--unit"></a>Ausgabe: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit) 

Ein neuer Vorgang, der $U ^ m $ darstellt, wobei $m = \texttt{Power} $ ist.

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ des Vorgangs, der eingeschaltet werden soll.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. operationpowc](xref:Microsoft.Quantum.Canon.OperationPowC)
- [Microsoft. Quantum. Canon. operationpowa](xref:Microsoft.Quantum.Canon.OperationPowA)
- [Microsoft. Quantum. Canon. operationpowca](xref:Microsoft.Quantum.Canon.OperationPowCA)
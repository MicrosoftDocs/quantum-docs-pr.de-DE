---
uid: Microsoft.Quantum.Canon.OperationPowA
title: Operationpowa-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: OperationPowA
qsharp.summary: >-
  Raises an operation to a power. The modifier `A` indicates that the operation is adjointable.

  That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.
ms.openlocfilehash: 66df354c6de7e48624712276882759043b78466c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703931"
---
# <a name="operationpowa-function"></a>Operationpowa-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Löst einen Vorgang für eine Stromversorgung aus.
Der-Modifizierer `A` gibt an, dass der Vorgang adjointable ist.

Das heißt, wenn ein Vorgang, der ein Gate $U $ darstellt, einen neuen Vorgang $U ^ m $ für eine Power $m $ zurückgibt.

```qsharp
function OperationPowA<'T> (op : ('T => Unit is Adj), power : Int) : ('T => Unit is Adj)
```


## <a name="input"></a>Eingabe

### <a name="op--t--unit-adj"></a>OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ

Ein Vorgang $U $, der das Gate darstellt, das wiederholt werden soll.


### <a name="power--int"></a>Power: [int](xref:microsoft.quantum.lang-ref.int)

Gibt an, wie oft $U $ wiederholt werden soll.



## <a name="output--t--unit-adj"></a>Ausgabe: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ

Ein neuer Vorgang, der $U ^ m $ darstellt, wobei $m = \texttt{Power} $ ist.

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ des Vorgangs, der eingeschaltet werden soll.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. operationpow](xref:Microsoft.Quantum.Canon.OperationPow)
---
uid: Microsoft.Quantum.Canon.OperationPowCA
title: Operationpowca-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: OperationPowCA
qsharp.summary: >-
  Raises an operation to a power. The modifier `A` indicates that the operation is controllable and adjointable.

  That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.
ms.openlocfilehash: 753063452616747309e3e228ce8a702f4378c61f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703913"
---
# <a name="operationpowca-function"></a>Operationpowca-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Löst einen Vorgang für eine Stromversorgung aus.
Der-Modifizierer `A` gibt an, dass der Vorgang steuerbar und adjointable ist.

Das heißt, wenn ein Vorgang, der ein Gate $U $ darstellt, einen neuen Vorgang $U ^ m $ für eine Power $m $ zurückgibt.

```qsharp
function OperationPowCA<'T> (op : ('T => Unit is Ctl + Adj), power : Int) : ('T => Unit is Ctl + Adj)
```


## <a name="input"></a>Eingabe

### <a name="op--t--unit-ctl--adj"></a>OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL + ADJ

Ein Vorgang $U $, der das Gate darstellt, das wiederholt werden soll.


### <a name="power--int"></a>Power: [int](xref:microsoft.quantum.lang-ref.int)

Gibt an, wie oft $U $ wiederholt werden soll.



## <a name="output--t--unit-ctl--adj"></a>Ausgabe: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL + ADJ

Ein neuer Vorgang, der $U ^ m $ darstellt, wobei $m = \texttt{Power} $ ist.

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ des Vorgangs, der eingeschaltet werden soll.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. operationpow](xref:Microsoft.Quantum.Canon.OperationPow)
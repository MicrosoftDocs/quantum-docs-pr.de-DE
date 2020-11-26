---
uid: Microsoft.Quantum.Canon.OperationPowC
title: Operationpowc-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: OperationPowC
qsharp.summary: >-
  Raises an operation to a power. The modifier `C` indicates that the operation is controllable.

  That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.
ms.openlocfilehash: 71f66dd0098ab58d327fc33dbe5af191df0d3dc3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205727"
---
# <a name="operationpowc-function"></a>Operationpowc-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Löst einen Vorgang für eine Stromversorgung aus.
Der-Modifizierer `C` gibt an, dass der Vorgang steuerbar ist.

Das heißt, wenn ein Vorgang, der ein Gate $U $ darstellt, einen neuen Vorgang $U ^ m $ für eine Power $m $ zurückgibt.

```qsharp
function OperationPowC<'T> (op : ('T => Unit is Ctl), power : Int) : ('T => Unit is Ctl)
```


## <a name="input"></a>Eingabe

### <a name="op--t--unit--is-ctl"></a>OP: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL

Ein Vorgang $U $, der das Gate darstellt, das wiederholt werden soll.


### <a name="power--int"></a>Power: [int](xref:microsoft.quantum.lang-ref.int)

Gibt an, wie oft $U $ wiederholt werden soll.



## <a name="output--t--unit--is-ctl"></a>Ausgabe: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL

Ein neuer Vorgang, der $U ^ m $ darstellt, wobei $m = \texttt{Power} $ ist.

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ des Vorgangs, der eingeschaltet werden soll.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. operationpow](xref:Microsoft.Quantum.Canon.OperationPow)
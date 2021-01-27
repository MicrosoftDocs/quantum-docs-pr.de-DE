---
uid: Microsoft.Quantum.Canon.OperationPowA
title: Operationpowa-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: OperationPowA
qsharp.summary: >-
  Raises an operation to a power. The modifier `A` indicates that the operation is adjointable.

  That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.
ms.openlocfilehash: 67491c3302392e9793677727606df1baaf4f205a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852359"
---
# <a name="operationpowa-function"></a>Operationpowa-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Löst einen Vorgang für eine Stromversorgung aus.
Der-Modifizierer `A` gibt an, dass der Vorgang adjointable ist.

Das heißt, wenn ein Vorgang, der ein Gate $U $ darstellt, einen neuen Vorgang $U ^ m $ für eine Power $m $ zurückgibt.

```qsharp
function OperationPowA<'T> (op : ('T => Unit is Adj), power : Int) : ('T => Unit is Adj)
```


## <a name="input"></a>Eingabe

### <a name="op--t--unit--is-adj"></a>OP: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ

Ein Vorgang $U $, der das Gate darstellt, das wiederholt werden soll.


### <a name="power--int"></a>Power: [int](xref:microsoft.quantum.lang-ref.int)

Gibt an, wie oft $U $ wiederholt werden soll.



## <a name="output--t--unit--is-adj"></a>Ausgabe: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ

Ein neuer Vorgang, der $U ^ m $ darstellt, wobei $m = \texttt{Power} $ ist.

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ des Vorgangs, der eingeschaltet werden soll.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. operationpow](xref:Microsoft.Quantum.Canon.OperationPow)
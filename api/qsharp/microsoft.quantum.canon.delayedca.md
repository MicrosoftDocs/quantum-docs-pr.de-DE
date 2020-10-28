---
uid: Microsoft.Quantum.Canon.DelayedCA
title: Delayedca-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayedCA
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: 8ee55e2ca7ec2cff9618b5dc66e19d88779d39ce
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704199"
---
# <a name="delayedca-function"></a>Delayedca-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Gibt einen Vorgang zurück, der den angegebenen Vorgang mit dem angegebenen Argument anwendet.

```qsharp
function DelayedCA<'T> (op : ('T => Unit is Ctl + Adj), arg : 'T) : (Unit => Unit is Ctl + Adj)
```


## <a name="input"></a>Eingabe

### <a name="op--t--unit-ctl--adj"></a>OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL + ADJ

Ein Vorgang, der als Ergebnis der Anwendung eines Rückgabewerts angewendet werden soll.


### <a name="arg--t"></a>arg: 't

Die Eingabe, auf die der Vorgang `op` angewendet wird.



## <a name="output--unit--unit-ctl--adj"></a>Ausgabe: [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL + ADJ

Ein neuer Vorgang, der `op` mit Input angewendet wird. `arg`

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Eingabetyp des Vorgangs, der verzögert werden soll.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. verzögert](xref:Microsoft.Quantum.Canon.Delayed)
- [Microsoft. Quantum. Canon. Delay](xref:Microsoft.Quantum.Canon.Delay)
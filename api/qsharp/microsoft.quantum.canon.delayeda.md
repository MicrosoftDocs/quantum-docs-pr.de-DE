---
uid: Microsoft.Quantum.Canon.DelayedA
title: Delayeda-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayedA
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: 33ff4dab36a6c6e17b9496a623f70b814c9f2fed
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207070"
---
# <a name="delayeda-function"></a>Delayeda-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt einen Vorgang zurück, der den angegebenen Vorgang mit dem angegebenen Argument anwendet.

```qsharp
function DelayedA<'T> (op : ('T => Unit is Adj), arg : 'T) : (Unit => Unit is Adj)
```


## <a name="input"></a>Eingabe

### <a name="op--t--unit--is-adj"></a>OP: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ

Ein Vorgang, der als Ergebnis der Anwendung eines Rückgabewerts angewendet werden soll.


### <a name="arg--t"></a>arg: 't

Die Eingabe, auf die der Vorgang `op` angewendet wird.



## <a name="output--unit--unit--is-adj"></a>Ausgabe: [Einheiten](xref:microsoft.quantum.lang-ref.unit) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ

Ein neuer Vorgang, der `op` mit Input angewendet wird. `arg`

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Eingabetyp des Vorgangs, der verzögert werden soll.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. verzögert](xref:Microsoft.Quantum.Canon.Delayed)
- [Microsoft. Quantum. Canon. Delay](xref:Microsoft.Quantum.Canon.Delay)
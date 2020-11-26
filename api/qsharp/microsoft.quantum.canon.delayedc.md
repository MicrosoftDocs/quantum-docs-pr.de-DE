---
uid: Microsoft.Quantum.Canon.DelayedC
title: Delayedc-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayedC
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: d8036397559b1587b806f701d89e892eea2da8f9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207009"
---
# <a name="delayedc-function"></a>Delayedc-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt einen Vorgang zurück, der den angegebenen Vorgang mit dem angegebenen Argument anwendet.

```qsharp
function DelayedC<'T> (op : ('T => Unit is Ctl), arg : 'T) : (Unit => Unit is Ctl)
```


## <a name="input"></a>Eingabe

### <a name="op--t--unit--is-ctl"></a>OP: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL

Ein Vorgang, der als Ergebnis der Anwendung eines Rückgabewerts angewendet werden soll.


### <a name="arg--t"></a>arg: 't

Die Eingabe, auf die der Vorgang `op` angewendet wird.



## <a name="output--unit--unit--is-ctl"></a>Ausgabe: [Einheiten](xref:microsoft.quantum.lang-ref.unit) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL

Ein neuer Vorgang, der `op` mit Input angewendet wird. `arg`

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Eingabetyp des Vorgangs, der verzögert werden soll.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. verzögert](xref:Microsoft.Quantum.Canon.Delayed)
- [Microsoft. Quantum. Canon. Delay](xref:Microsoft.Quantum.Canon.Delay)
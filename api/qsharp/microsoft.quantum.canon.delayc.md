---
uid: Microsoft.Quantum.Canon.DelayC
title: Delta-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayC
qsharp.summary: Applies a given operation with a delay.
ms.openlocfilehash: acb817c3322063353dc08c5d6f8c539391b3bf39
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704239"
---
# <a name="delayc-operation"></a>Delta-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Wendet einen angegebenen Vorgang mit einer Verzögerung an.

```qsharp
operation DelayC<'T> (op : ('T => Unit is Ctl), arg : 'T, aux : Unit) : Unit
```


## <a name="description"></a>BESCHREIBUNG

Wenn ein Vorgang und eine Eingabe für diesen Vorgang vorhanden sind, wendet den Vorgang an, sobald eine zusätzliche Eingabe bereitgestellt wird.
Der-Ausdruck ist insbesondere `Delay(op, arg, _)` ein Vorgang, der `op` sich auf bezieht, `arg` Wenn aufgerufen wird.
`Delay(op,arg,_)`Der Ausdruck ermöglicht das Verzögern der Anwendung von `op` .

## <a name="input"></a>Eingabe

### <a name="op--t--unit-ctl"></a>OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL

Ein anzuwendende Vorgang.


### <a name="arg--t"></a>arg: 't

Die Eingabe, auf die der Vorgang angewendet wird.


### <a name="aux--unit"></a>AUX: [Unit](xref:microsoft.quantum.lang-ref.unit)

Argument, das verwendet wird, um die Anwendung des Vorgangs mithilfe der partiellen Anwendung zu verzögern.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Eingabetyp des Vorgangs, der verzögert werden soll.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. Delay](xref:Microsoft.Quantum.Canon.Delay)
- [Microsoft. Quantum. Canon. verzögert](xref:Microsoft.Quantum.Canon.Delayed)
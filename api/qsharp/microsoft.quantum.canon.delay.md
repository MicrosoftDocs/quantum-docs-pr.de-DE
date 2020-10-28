---
uid: Microsoft.Quantum.Canon.Delay
title: Verzögerungs Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Delay
qsharp.summary: Applies a given operation with a delay.
ms.openlocfilehash: f9f0e5c3120eb69bd7431d52d6cde5e846ffbe4d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704255"
---
# <a name="delay-operation"></a>Verzögerungs Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Wendet einen angegebenen Vorgang mit einer Verzögerung an.

```qsharp
operation Delay<'T, 'U> (op : ('T => 'U), arg : 'T, aux : Unit) : 'U
```


## <a name="description"></a>BESCHREIBUNG

Wenn ein Vorgang und eine Eingabe für diesen Vorgang vorhanden sind, wendet den Vorgang an, sobald eine zusätzliche Eingabe bereitgestellt wird.
Der-Ausdruck ist insbesondere `Delay(op, arg, _)` ein Vorgang, der `op` sich auf bezieht, `arg` Wenn aufgerufen wird.
`Delay(op,arg,_)`Der Ausdruck ermöglicht das Verzögern der Anwendung von `op` .

## <a name="input"></a>Eingabe

### <a name="op--t--u"></a>OP: 't => ' U 

Ein anzuwendende Vorgang.


### <a name="arg--t"></a>arg: 't

Die Eingabe, auf die der Vorgang angewendet wird.


### <a name="aux--unit"></a>AUX: [Unit](xref:microsoft.quantum.lang-ref.unit)

Argument, das verwendet wird, um die Anwendung des Vorgangs mithilfe der partiellen Anwendung zu verzögern.



## <a name="output--u"></a>Ausgabe: "U



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Eingabetyp des Vorgangs, der verzögert werden soll.
### <a name="u"></a>"U

Der Rückgabetyp des Vorgangs, der verzögert werden soll.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. Delta-c](xref:Microsoft.Quantum.Canon.DelayC)
- [Microsoft. Quantum. Canon. Delaya](xref:Microsoft.Quantum.Canon.DelayA)
- [Microsoft. Quantum. Canon. Delta-ca](xref:Microsoft.Quantum.Canon.DelayCA)
- [Microsoft. Quantum. Canon. verzögert](xref:Microsoft.Quantum.Canon.Delayed)
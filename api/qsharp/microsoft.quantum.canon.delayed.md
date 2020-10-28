---
uid: Microsoft.Quantum.Canon.Delayed
title: Verzögerte Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Delayed
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: 820a38c2b4de2e0151d55bd88fb4f69567182f6b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704218"
---
# <a name="delayed-function"></a>Verzögerte Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Gibt einen Vorgang zurück, der den angegebenen Vorgang mit dem angegebenen Argument anwendet.

```qsharp
function Delayed<'T, 'U> (op : ('T => 'U), arg : 'T) : (Unit => 'U)
```


## <a name="input"></a>Eingabe

### <a name="op--t--u"></a>OP: 't => ' U 

Ein anzuwendende Vorgang.


### <a name="arg--t"></a>arg: 't

Die Eingabe, auf die der Vorgang angewendet wird.



## <a name="output--unit--u"></a>Ausgabe: [Unit](xref:microsoft.quantum.lang-ref.unit) => ' U 

Ein neuer Vorgang, der `op` mit Input angewendet wird. `arg`

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Eingabetyp des Vorgangs, der verzögert werden soll.
### <a name="u"></a>"U

Der Rückgabetyp des Vorgangs, der verzögert werden soll.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. delayedc](xref:Microsoft.Quantum.Canon.DelayedC)
- [Microsoft. Quantum. Canon. delayeda](xref:Microsoft.Quantum.Canon.DelayedA)
- [Microsoft. Quantum. Canon. delayedca](xref:Microsoft.Quantum.Canon.DelayedCA)
- [Microsoft. Quantum. Canon. Delay](xref:Microsoft.Quantum.Canon.Delay)
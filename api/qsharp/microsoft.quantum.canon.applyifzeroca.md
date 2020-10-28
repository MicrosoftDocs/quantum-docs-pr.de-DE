---
uid: Microsoft.Quantum.Canon.ApplyIfZeroCA
title: Applyif nuloca-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfZeroCA
qsharp.summary: Applies a unitary operation conditioned on a classical result value being zero.
ms.openlocfilehash: 85612bd3dd7af45b7901fef775a7d556eb229608
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705218"
---
# <a name="applyifzeroca-operation"></a>Applyif nuloca-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Wendet einen einheitlichen Vorgang an, der auf einem klassischen Ergebniswert von 0 (null) liegt.

```qsharp
operation ApplyIfZeroCA<'T> (result : Result, (op : ('T => Unit is Adj + Ctl), target : 'T)) : Unit
```


## <a name="description"></a>BESCHREIBUNG

Bei einem Vorgang `op` und einem Ergebniswert `result` gilt `op` für, `target` wenn gleich `result` ist `Zero` . Gibt `One` an, dass nichts passiert `target` .
Das-Suffix `CA` gibt an, dass der anzuwendende Vorgang einheitlich (steuerbar und adjointable) ist.

## <a name="input"></a>Eingabe

### <a name="result--__invalidresult__"></a>Ergebnis: __ungültig <Result>__

Ein Messergebnis, das steuert, ob op angewendet wird.


### <a name="op--t--unit-adj--ctl"></a>OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL

Ein Vorgang, der bedingt angewendet werden soll.


### <a name="target--t"></a>Ziel: 't

Die Eingabe, auf die der Vorgang angewendet wird.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Eingabetyp des Vorgangs, der bedingt angewendet werden soll.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. applyif zeroc](xref:Microsoft.Quantum.Canon.ApplyIfZeroC)
- [Microsoft. Quantum. Canon. applyif zeroa](xref:Microsoft.Quantum.Canon.ApplyIfZeroA)
- [Microsoft. Quantum. Canon. applyif nuloca](xref:Microsoft.Quantum.Canon.ApplyIfZeroCA)
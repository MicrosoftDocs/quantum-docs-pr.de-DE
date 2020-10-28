---
uid: Microsoft.Quantum.Canon.ApplyIfZeroA
title: Applyif zeroa-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfZeroA
qsharp.summary: Applies an adjointable operation conditioned on a classical result value being zero.
ms.openlocfilehash: d324cd970e8df49ceb51b6bf5c9f3c9c3ff142f9
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705247"
---
# <a name="applyifzeroa-operation"></a>Applyif zeroa-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Wendet einen adjointable-Vorgang an, der von einem klassischen Ergebniswert von 0 (null) abhängt.

```qsharp
operation ApplyIfZeroA<'T> (result : Result, (op : ('T => Unit is Adj), target : 'T)) : Unit
```


## <a name="description"></a>BESCHREIBUNG

Bei einem Vorgang `op` und einem Ergebniswert `result` gilt `op` für, `target` wenn gleich `result` ist `Zero` . Gibt `One` an, dass nichts passiert `target` .
Das-Suffix `A` gibt an, dass der anzuwendende Vorgang adjointable ist.

## <a name="input"></a>Eingabe

### <a name="result--__invalidresult__"></a>Ergebnis: __ungültig <Result>__

Ein Messergebnis, das steuert, ob op angewendet wird.


### <a name="op--t--unit-adj"></a>OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ

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
---
uid: Microsoft.Quantum.Canon.ApplyIfA
title: Applyifa-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfA
qsharp.summary: Applies a adjointable operation conditioned on a classical bit.
ms.openlocfilehash: 279a069176ee24ed83406f72170462bf58c790d9
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705362"
---
# <a name="applyifa-operation"></a>Applyifa-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Wendet einen adjointable-Vorgang an, der auf einem klassischen Bit bedingt ist.

```qsharp
operation ApplyIfA<'T> (op : ('T => Unit is Adj), bit : Bool, target : 'T) : Unit
```


## <a name="description"></a>BESCHREIBUNG

Bei einem Vorgang `op` und einem Bitwert `bit` gilt für `op` das, `target` wenn gleich `bit` ist `true` . Gibt `false` an, dass nichts passiert `target` .
Das-Suffix `A` gibt an, dass der anzuwendende Vorgang adjointable ist.

## <a name="input"></a>Eingabe

### <a name="op--t--unit-adj"></a>OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ

Ein Vorgang, der bedingt angewendet werden soll.


### <a name="bit--bool"></a>Bit: [bool](xref:microsoft.quantum.lang-ref.bool)

ein boolescher Wert, der steuert, ob op angewendet wird.


### <a name="target--t"></a>Ziel: 't

Die Eingabe, auf die der Vorgang angewendet wird.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Eingabetyp des Vorgangs, der bedingt angewendet werden soll.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. applyifc](xref:Microsoft.Quantum.Canon.ApplyIfC)
- [Microsoft. Quantum. Canon. applyifa](xref:Microsoft.Quantum.Canon.ApplyIfA)
- [Microsoft. Quantum. Canon. applyifca](xref:Microsoft.Quantum.Canon.ApplyIfCA)
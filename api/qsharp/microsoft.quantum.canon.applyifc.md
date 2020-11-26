---
uid: Microsoft.Quantum.Canon.ApplyIfC
title: Applyifc-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfC
qsharp.summary: Applies a controllable operation conditioned on a classical bit.
ms.openlocfilehash: 35430cb7cf491965b7b69ace6d3f41599dbadd51
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218715"
---
# <a name="applyifc-operation"></a>Applyifc-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Wendet eine steuerbare Operation an, die auf einem klassischen Bit bedingt ist.

```qsharp
operation ApplyIfC<'T> (op : ('T => Unit is Ctl), bit : Bool, target : 'T) : Unit is Ctl
```


## <a name="description"></a>BESCHREIBUNG

Bei einem Vorgang `op` und einem Bitwert `bit` gilt für `op` das, `target` wenn gleich `bit` ist `true` . Gibt `false` an, dass nichts passiert `target` .
Das-Suffix `C` gibt an, dass der anzuwendende Vorgang steuerbar ist.

## <a name="input"></a>Eingabe

### <a name="op--t--unit--is-ctl"></a>OP: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL

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
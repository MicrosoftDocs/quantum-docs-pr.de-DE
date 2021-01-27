---
uid: Microsoft.Quantum.Canon.ApplyIfC
title: Applyifc-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfC
qsharp.summary: Applies a controllable operation conditioned on a classical bit.
ms.openlocfilehash: ef16b23349b604d174e72d9ae06d2052e2ab60f8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841856"
---
# <a name="applyifc-operation"></a>Applyifc-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Wendet eine steuerbare Operation an, die auf einem klassischen Bit bedingt ist.

```qsharp
operation ApplyIfC<'T> (op : ('T => Unit is Ctl), bit : Bool, target : 'T) : Unit is Ctl
```


## <a name="description"></a>Beschreibung

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

## <a name="example"></a>Beispiel

Im folgenden wird ein Register von Qubits auf einen Berechnungs Status vorbereitet, der durch eine klassische Bitzeichenfolge dargestellt wird, die als Array von Werten angegeben ist `Bool` :

```qsharp
let bitstring = [true, false, true];
using (register = Qubit(3)) {
    ApplyToEach(ApplyIf(X, _, _), Zipped(bitstring, register));
    // register should now be in the state |101⟩.
    ...
}
```

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. applyifc](xref:Microsoft.Quantum.Canon.ApplyIfC)
- [Microsoft. Quantum. Canon. applyifa](xref:Microsoft.Quantum.Canon.ApplyIfA)
- [Microsoft. Quantum. Canon. applyifca](xref:Microsoft.Quantum.Canon.ApplyIfCA)
---
uid: Microsoft.Quantum.Canon.ApplyIfElseBC
title: Applyifeleinbc-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseBC
qsharp.summary: Applies one of two controllable operations, depending on the value of a classical bit.
ms.openlocfilehash: 032d92484dc96481cb981d9d8acfeed248a9116d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705338"
---
# <a name="applyifelsebc-operation"></a>Applyifeleinbc-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Wendet je nach dem Wert eines klassischen Bits einen von zwei kontrollierbaren Vorgängen an.

```qsharp
operation ApplyIfElseBC<'T, 'U> (bit : Bool, (trueOp : ('T => Unit is Ctl), trueInput : 'T), (falseOp : ('U => Unit is Ctl), falseInput : 'U)) : Unit
```


## <a name="description"></a>BESCHREIBUNG

Wenn ein Bit angegeben ist `bit` , wendet den Vorgang `trueOp` mit `trueInput` als Eingabe an, wenn den Wert `bit` `true` hat, und gilt, wenn den Wert hat `falseOp(falseInput)` `bit` `false` .

## <a name="input"></a>Eingabe

### <a name="bit--bool"></a>Bit: [bool](xref:microsoft.quantum.lang-ref.bool)

Der boolesche Wert, der verwendet wird, um zu bestimmen, ob `trueOp` oder `falseOp` angewendet wird.


### <a name="trueop--t--unit-ctl"></a>trueop: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL

Der zu verwendende kontrollierbare Vorgang, wenn `bit` ist `true` .


### <a name="trueinput--t"></a>trueinput: 't

Die Eingabe, die für bereitgestellt werden soll, `trueOp` Wenn `bit` ist `true` .


### <a name="falseop--u--unit-ctl"></a>falseop: "U => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL

Der zu verwendende kontrollierbare Vorgang, wenn `bit` ist `false` .


### <a name="falseinput--u"></a>falseinput: ' U

Die Eingabe, die für bereitgestellt werden soll, `falseOp` Wenn `bit` ist `false` .



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Eingabetyp des Vorgangs `trueOp` , der bedingt angewendet werden soll.
### <a name="u"></a>"U

Der Eingabetyp des Vorgangs `falseOp` , der bedingt angewendet werden soll.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. applyif Zero](xref:Microsoft.Quantum.Canon.ApplyIfZero)
- [Microsoft. Quantum. Canon. applyifone](xref:Microsoft.Quantum.Canon.ApplyIfOne)
- [Microsoft. Quantum. Canon. applyifelserc](xref:Microsoft.Quantum.Canon.ApplyIfElseRC)
- [Microsoft. Quantum. Canon. applyifelsera](xref:Microsoft.Quantum.Canon.ApplyIfElseRA)
- [Microsoft. Quantum. Canon. applyifelserca](xref:Microsoft.Quantum.Canon.ApplyIfElseRCA)
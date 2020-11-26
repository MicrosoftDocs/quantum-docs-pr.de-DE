---
uid: Microsoft.Quantum.Canon.ApplyIfElseRC
title: Applyifelserc-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseRC
qsharp.summary: Applies one of two controllable operations, depending on the value of a classical result.
ms.openlocfilehash: b2e4ade84b25b0100fe4b69814c760a672833f06
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209484"
---
# <a name="applyifelserc-operation"></a>Applyifelserc-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Wendet je nach dem Wert eines klassischen Ergebnisses einen von zwei kontrollierbaren Vorgängen an.

```qsharp
operation ApplyIfElseRC<'T, 'U> (result : Result, (zeroOp : ('T => Unit is Ctl), zeroInput : 'T), (oneOp : ('U => Unit is Ctl), oneInput : 'U)) : Unit is Ctl
```


## <a name="description"></a>BESCHREIBUNG

Bei einem Ergebnis `result` wendet den Vorgang `zeroOp` mit `zeroInput` als Eingabe an, wenn `result` gleich ist `Zero` , und gilt, wenn gleich ist `oneOp(oneInput)` `result == One` .

## <a name="input"></a>Eingabe

### <a name="result--__invalidresult__"></a>Ergebnis: __ungültig <Result>__

Das Messergebnis, mit dem bestimmt wird, ob `zeroOp` oder `oneOp` angewendet wird.


### <a name="zeroop--t--unit--is-ctl"></a>zeroop: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL

Der zu verwendende kontrollierbare Vorgang, wenn `result == Zero` .


### <a name="zeroinput--t"></a>NULL-Eingabe: 't

Die Eingabe, die für bereitgestellt werden soll `zeroOp` `result == Zero` .


### <a name="oneop--u--unit--is-ctl"></a>oneop: "U => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL

Der zu verwendende kontrollierbare Vorgang, wenn `result == One` .


### <a name="oneinput--u"></a>oneinput: ' U

Die Eingabe, die für bereitgestellt werden soll `oneOp` `result == One` .



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Eingabetyp des Vorgangs `zeroOp` , der bedingt angewendet werden soll.
### <a name="u"></a>"U

Der Eingabetyp des Vorgangs `oneOp` , der bedingt angewendet werden soll.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. applyif Zero](xref:Microsoft.Quantum.Canon.ApplyIfZero)
- [Microsoft. Quantum. Canon. applyifone](xref:Microsoft.Quantum.Canon.ApplyIfOne)
- [Microsoft. Quantum. Canon. applyifelserc](xref:Microsoft.Quantum.Canon.ApplyIfElseRC)
- [Microsoft. Quantum. Canon. applyifelsera](xref:Microsoft.Quantum.Canon.ApplyIfElseRA)
- [Microsoft. Quantum. Canon. applyifelserca](xref:Microsoft.Quantum.Canon.ApplyIfElseRCA)
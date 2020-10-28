---
uid: Microsoft.Quantum.Canon.ApplyToElementCA
title: Applydeelementca-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToElementCA
qsharp.summary: Applies an operation to a given element of an array.
ms.openlocfilehash: 599a8afe1ab97b0ab0d6621cabd7707faaeddda3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704898"
---
# <a name="applytoelementca-operation"></a>Applydeelementca-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Wendet einen Vorgang auf ein angegebenes Element eines Arrays an.

```qsharp
operation ApplyToElementCA<'T> (op : ('T => Unit is Adj + Ctl), index : Int, targets : 'T[]) : Unit
```


## <a name="description"></a>BESCHREIBUNG

Wenn ein Vorgang `op` , ein Index `index` und ein Array von Zielen `targets` , gilt, gilt `op(targets[index])` .

## <a name="input"></a>Eingabe

### <a name="op--t--unit-adj--ctl"></a>OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL

Ein anzuwendende Vorgang.


### <a name="index--int"></a>Index: [int](xref:microsoft.quantum.lang-ref.int)

Ein Index in das Array von Zielen.


### <a name="targets--t"></a>Ziele: 't []

Ein Array möglicher Ziele für `op` .



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Eingabetyp des Vorgangs, der angewendet werden soll.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. applyyelement](xref:Microsoft.Quantum.Canon.ApplyToElement)
- [Microsoft. Quantum. Canon. applyyelementc](xref:Microsoft.Quantum.Canon.ApplyToElementC)
- [Microsoft. Quantum. Canon. applyyelementa](xref:Microsoft.Quantum.Canon.ApplyToElementA)
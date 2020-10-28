---
uid: Microsoft.Quantum.Canon.ApplyToElement
title: Applydeelement-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToElement
qsharp.summary: Applies an operation to a given element of an array.
ms.openlocfilehash: 5c321d95c9b79bc50827c2b50c406b164e143dc6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704935"
---
# <a name="applytoelement-operation"></a>Applydeelement-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Wendet einen Vorgang auf ein angegebenes Element eines Arrays an.

```qsharp
operation ApplyToElement<'T> (op : ('T => Unit), index : Int, targets : 'T[]) : Unit
```


## <a name="description"></a>BESCHREIBUNG

Wenn ein Vorgang `op` , ein Index `index` und ein Array von Zielen `targets` , gilt, gilt `op(targets[index])` .

## <a name="input"></a>Eingabe

### <a name="op--t--unit"></a>OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) 

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

- [Microsoft. Quantum. Canon. applyyelementc](xref:Microsoft.Quantum.Canon.ApplyToElementC)
- [Microsoft. Quantum. Canon. applyyelementa](xref:Microsoft.Quantum.Canon.ApplyToElementA)
- [Microsoft. Quantum. Canon. applyyelementca](xref:Microsoft.Quantum.Canon.ApplyToElementCA)
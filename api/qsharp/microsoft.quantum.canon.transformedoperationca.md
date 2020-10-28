---
uid: Microsoft.Quantum.Canon.TransformedOperationCA
title: Transformedoperationca-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TransformedOperationCA
qsharp.summary: Given a function and an operation, returns a new operation whose input is transformed by the given function.
ms.openlocfilehash: 21c9cdfc3b5b266cb3b93e52ee2fa4c655caf795
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703758"
---
# <a name="transformedoperationca-function"></a>Transformedoperationca-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Gibt bei Angabe einer Funktion und eines Vorgangs einen neuen Vorgang zurück, dessen Eingabe von der angegebenen Funktion transformiert wird.

```qsharp
function TransformedOperationCA<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit is Adj + Ctl)) : ('U => Unit is Adj + Ctl)
```


## <a name="input"></a>Eingabe

### <a name="fn--u---t"></a>FN: ' U-> 't

Eine Funktion, die die angegebene Eingabe in ein vom Vorgang erwartetes Formular umwandelt.


### <a name="op--t--unit-adj--ctl"></a>OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL

Der Vorgang, der transformiert werden soll.



## <a name="output--u--unit-adj--ctl"></a>Ausgabe: "U => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL

Ein neuer Vorgang `fn` , den tbat mit seiner Eingabe aufruft, übergibt die resultierende Ausgabe anschließend an `op` .

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF


### <a name="u"></a>"U



## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. transformedoperation](xref:Microsoft.Quantum.Canon.TransformedOperation)
- [Microsoft. Quantum. Canon. transformedoperationa](xref:Microsoft.Quantum.Canon.TransformedOperationA)
- [Microsoft. Quantum. Canon. transformedoperationca](xref:Microsoft.Quantum.Canon.TransformedOperationCA)
- [Microsoft. Quantum. Canon. applywithinputtransformation](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [Microsoft. Quantum. Canon. verfasst](xref:Microsoft.Quantum.Canon.Composed)
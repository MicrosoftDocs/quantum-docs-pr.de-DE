---
uid: Microsoft.Quantum.Canon.TransformedOperationCA
title: Transformedoperationca-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TransformedOperationCA
qsharp.summary: Given a function and an operation, returns a new operation whose input is transformed by the given function.
ms.openlocfilehash: bb39530ae28e17d07a6a5c2bb2d35f81be312d15
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840121"
---
# <a name="transformedoperationca-function"></a>Transformedoperationca-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt bei Angabe einer Funktion und eines Vorgangs einen neuen Vorgang zurück, dessen Eingabe von der angegebenen Funktion transformiert wird.

```qsharp
function TransformedOperationCA<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit is Adj + Ctl)) : ('U => Unit is Adj + Ctl)
```


## <a name="input"></a>Eingabe

### <a name="fn--u---t"></a>FN: ' U-> 't

Eine Funktion, die die angegebene Eingabe in ein vom Vorgang erwartetes Formular umwandelt.


### <a name="op--t--unit--is-adj--ctl"></a>OP: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL

Der Vorgang, der transformiert werden soll.



## <a name="output--u--unit--is-adj--ctl"></a>Ausgabe: "U => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL

Ein neuer Vorgang `fn` , den tbat mit seiner Eingabe aufruft, übergibt die resultierende Ausgabe anschließend an `op` .

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF


### <a name="u"></a>"U



## <a name="example"></a>Beispiel

Der folgende-Befehl verwendet @"Microsoft.Quantum.Arithmetic.LittleEndianAsBigEndian" , um einen für Eingaben entworfenen Vorgang @"Microsoft.Quantum.Arithmetic.BigEndian" in einen Vorgang umzuwandeln, der Eingaben vom Typ akzeptiert @"Microsoft.Quantum.Arithmetic.LittleEndian" :

```qsharp
let leOp = TransformedOperation(LittleEndianAsBigEndian, ApplyXorInPlaceBE);
```

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. transformedoperation](xref:Microsoft.Quantum.Canon.TransformedOperation)
- [Microsoft. Quantum. Canon. transformedoperationa](xref:Microsoft.Quantum.Canon.TransformedOperationA)
- [Microsoft. Quantum. Canon. transformedoperationca](xref:Microsoft.Quantum.Canon.TransformedOperationCA)
- [Microsoft. Quantum. Canon. applywithinputtransformation](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [Microsoft. Quantum. Canon. verfasst](xref:Microsoft.Quantum.Canon.Composed)
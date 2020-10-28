---
uid: Microsoft.Quantum.Canon.CControlledA
title: Ccontrolleda-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CControlledA
qsharp.summary: Given an operation op, returns a new operation which applies the op if a classical control bit is true. If `false`, nothing happens. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: 30b5e3408fa6e5a79b2f3d63cccc11899c0405ef
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704407"
---
# <a name="ccontrolleda-function"></a>Ccontrolleda-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Gibt bei einem Vorgang op einen neuen Vorgang zurück, der das OP anwendet, wenn ein klassisches Steuerelement "true" ist. Gibt an `false` , dass nichts passiert.
Der-Modifizierer `A` gibt an, dass der Vorgang adjointable ist.

```qsharp
function CControlledA<'T> (op : ('T => Unit is Adj)) : ((Bool, 'T) => Unit is Adj)
```


## <a name="input"></a>Eingabe

### <a name="op--t--unit-adj"></a>OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ

Ein Vorgang, der bedingt angewendet werden soll.



## <a name="output--boolt--unit-adj"></a>Ausgabe: ([bool](xref:microsoft.quantum.lang-ref.bool), 't) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ

Ein neuer Vorgang, bei dem es sich um einen op-Vorgang handelt, wenn das klassische Steuerelement

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Eingabetyp des Vorgangs, der bedingt angewendet werden soll.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. ckontrollierten](xref:Microsoft.Quantum.Canon.CControlled)
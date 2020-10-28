---
uid: Microsoft.Quantum.Canon.CControlled
title: C-gesteuerte Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CControlled
qsharp.summary: Given an operation op, returns a new operation which applies the op if a classical control bit is true. If `false`, nothing happens.
ms.openlocfilehash: a155b00806b17258b3f87629659bc7d786e4e11d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704410"
---
# <a name="ccontrolled-function"></a>C-gesteuerte Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Gibt bei einem Vorgang op einen neuen Vorgang zurück, der das OP anwendet, wenn ein klassisches Steuerelement "true" ist. Gibt an `false` , dass nichts passiert.

```qsharp
function CControlled<'T> (op : ('T => Unit)) : ((Bool, 'T) => Unit)
```


## <a name="input"></a>Eingabe

### <a name="op--t--unit"></a>OP: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) 

Ein Vorgang, der bedingt angewendet werden soll.



## <a name="output--boolt--unit"></a>Ausgabe: ([bool](xref:microsoft.quantum.lang-ref.bool), 't) => [Einheit](xref:microsoft.quantum.lang-ref.unit) 

Ein neuer Vorgang, bei dem es sich um einen op-Vorgang handelt, wenn das klassische Steuerelement

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Eingabetyp des Vorgangs, der bedingt angewendet werden soll.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. ccontrolledc](xref:Microsoft.Quantum.Canon.CControlledC)
- [Microsoft. Quantum. Canon. ccontrolleda](xref:Microsoft.Quantum.Canon.CControlledA)
- [Microsoft. Quantum. Canon. ccontrolledca](xref:Microsoft.Quantum.Canon.CControlledCA)
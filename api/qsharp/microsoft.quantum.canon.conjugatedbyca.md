---
uid: Microsoft.Quantum.Canon.ConjugatedByCA
title: Konkanable-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ConjugatedByCA
qsharp.summary: Given outer and inner operations, returns a new operation that conjugates the inner operation by the outer operation.
ms.openlocfilehash: df29bcf555026bceb13d6896db12e13671a49b9f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704330"
---
# <a name="conjugatedbyca-function"></a>Konkanable-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Bei den äußeren und inneren Vorgängen wird ein neuer Vorgang zurückgegeben, der den inneren Vorgang durch den äußeren Vorgang konjugiert.

```qsharp
function ConjugatedByCA<'T> (outerOperation : ('T => Unit is Adj), innerOperation : ('T => Unit is Adj + Ctl)) : ('T => Unit is Adj + Ctl)
```


## <a name="input"></a>Eingabe

### <a name="outeroperation--t--unit-adj"></a>outeroperation: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ

Der Vorgang $U $, der für die konjugierte $V $ verwendet werden soll. Beachten Sie, dass der äußere Vorgang $U $ adjointable sein muss, aber nicht steuerbar sein muss.


### <a name="inneroperation--t--unit-adj--ctl"></a>inneroperation: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL

Der Vorgang $V $ konjugated.



## <a name="output--t--unit-adj--ctl"></a>Ausgabe: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL

Ein neuer Vorgang, dessen Aktion durch die einheitliche $U ^ {\dagger} V U $ dargestellt wird.

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ des Ziels, für das die einzelnen inneren und äußeren Operationen agieren.

## <a name="remarks"></a>Hinweise

Der äußere Vorgang wird immer als adjointable angenommen, er muss jedoch nicht steuerbar sein, damit der kombinierte Vorgang steuerbar ist.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. Kon.](xref:Microsoft.Quantum.Canon.ConjugatedByA)
- [Microsoft. Quantum.......](xref:Microsoft.Quantum.Canon.ConjugatedByC)
- [Microsoft. Quantum. Canon. konkanonische byca](xref:Microsoft.Quantum.Canon.ConjugatedByCA)
- [Microsoft. Quantum. Canon. applywith](xref:Microsoft.Quantum.Canon.ApplyWith)
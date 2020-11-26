---
uid: Microsoft.Quantum.Canon.ConjugatedByA
title: Konkanable-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ConjugatedByA
qsharp.summary: Given outer and inner operations, returns a new operation that conjugates the inner operation by the outer operation.
ms.openlocfilehash: eaa104039b857f0469ddc0aaba97698eca20860d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207342"
---
# <a name="conjugatedbya-function"></a>Konkanable-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Bei den äußeren und inneren Vorgängen wird ein neuer Vorgang zurückgegeben, der den inneren Vorgang durch den äußeren Vorgang konjugiert.

```qsharp
function ConjugatedByA<'T> (outerOperation : ('T => Unit is Adj), innerOperation : ('T => Unit is Adj)) : ('T => Unit is Adj)
```


## <a name="input"></a>Eingabe

### <a name="outeroperation--t--unit--is-adj"></a>outeroperation: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ

Der Vorgang $U $, der für die konjugierte $V $ verwendet werden soll. Beachten Sie, dass der äußere Vorgang $U $ adjointable sein muss, aber nicht steuerbar sein muss.


### <a name="inneroperation--t--unit--is-adj"></a>inneroperation: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ

Der Vorgang $V $ konjugated.



## <a name="output--t--unit--is-adj"></a>Ausgabe: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ

Ein neuer Vorgang, dessen Aktion durch die einheitliche $U ^ {\dagger} V U $ dargestellt wird.

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ des Ziels, für das die einzelnen inneren und äußeren Operationen agieren.

## <a name="remarks"></a>Bemerkungen

Der äußere Vorgang wird immer als adjointable angenommen, er muss jedoch nicht steuerbar sein, damit der kombinierte Vorgang steuerbar ist.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. Kon.](xref:Microsoft.Quantum.Canon.ConjugatedByA)
- [Microsoft. Quantum.......](xref:Microsoft.Quantum.Canon.ConjugatedByC)
- [Microsoft. Quantum. Canon. konkanonische byca](xref:Microsoft.Quantum.Canon.ConjugatedByCA)
- [Microsoft. Quantum. Canon. applywith](xref:Microsoft.Quantum.Canon.ApplyWith)
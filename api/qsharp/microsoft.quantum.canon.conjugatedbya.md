---
uid: Microsoft.Quantum.Canon.ConjugatedByA
title: Konkanable-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ConjugatedByA
qsharp.summary: Given outer and inner operations, returns a new operation that conjugates the inner operation by the outer operation.
ms.openlocfilehash: 141c42d335add85103e16598264f781f32ab80fc
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840848"
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
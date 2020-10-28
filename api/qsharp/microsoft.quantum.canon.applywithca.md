---
uid: Microsoft.Quantum.Canon.ApplyWithCA
title: Applywithca-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWithCA
qsharp.summary: Given two operations, applies one as conjugated with the other.
ms.openlocfilehash: abc62791416e78c1b2937a226327b71da8b8e288
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704578"
---
# <a name="applywithca-operation"></a>Applywithca-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Bei zwei Vorgängen wird eine als konjugated mit dem anderen angewendet.

```qsharp
operation ApplyWithCA<'T> (outerOperation : ('T => Unit is Adj), innerOperation : ('T => Unit is Adj + Ctl), target : 'T) : Unit
```


## <a name="description"></a>BESCHREIBUNG

Bei zwei Vorgängen, die durch einheitliche Operatoren $U $ und $V $ beschrieben werden, wendet Sie diese in der Sequenz $U ^ {\dagger} V U $ an. Das heißt, dieser Vorgang implementiert den einheitlichen Operator, der durch $V $-konjugated mit $U $ angegeben wird.

## <a name="input"></a>Eingabe

### <a name="outeroperation--t--unit-adj"></a>outeroperation: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ

Der Vorgang $U $, der für die konjugierte $V $ verwendet werden soll. Beachten Sie, dass der äußere Vorgang $U $ adjointable sein muss, aber nicht steuerbar sein muss.


### <a name="inneroperation--t--unit-adj--ctl"></a>inneroperation: 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL

Der Vorgang $V $ konjugated.


### <a name="target--t"></a>Ziel: 't

Die Eingabe, die für den äußeren und inneren Vorgang bereitgestellt werden soll.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Das Ziel, für das die einzelnen inneren und äußeren Operationen fungieren.

## <a name="remarks"></a>Hinweise

Der äußere Vorgang wird immer als adjointable angenommen, er muss jedoch nicht steuerbar sein, damit der kombinierte Vorgang steuerbar ist.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. applywith](xref:Microsoft.Quantum.Canon.ApplyWith)
- [Microsoft. Quantum. Canon. applyvon](xref:Microsoft.Quantum.Canon.ApplyWithA)
- [Microsoft. Quantum. Canon. applywithc](xref:Microsoft.Quantum.Canon.ApplyWithC)
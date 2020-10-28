---
uid: Microsoft.Quantum.Canon.RepeatCA
title: Repeatca-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RepeatCA
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: b68c3aa4298fffa76f7c43ac4c6d27cdf3b72fbf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703859"
---
# <a name="repeatca-operation"></a>Repeatca-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Wiederholt einen Vorgang mit einer angegebenen Anzahl von vorkommen.

```qsharp
operation RepeatCA<'TInput> (op : ('TInput => Unit is Adj + Ctl), nTimes : Int, input : 'TInput) : Unit
```


## <a name="input"></a>Eingabe

### <a name="op--tinput--unit-adj--ctl"></a>OP: ' TInput => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL

Der Vorgang, der wiederholt aufgerufen werden soll.


### <a name="ntimes--int"></a>nTimes: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der aufzurufenden Versuche `op` .


### <a name="input--tinput"></a>Eingabe: ' TInput

Die an zu über gebenden Eingaben `op` .



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Typparameter

### <a name="tinput"></a>' TInput



## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Arrays. drawmany](xref:Microsoft.Quantum.Arrays.DrawMany)
- [Microsoft. Quantum. Canon. Repeat](xref:Microsoft.Quantum.Canon.Repeat)
- [Microsoft. Quantum. Canon. repeata](xref:Microsoft.Quantum.Canon.RepeatA)
- [Microsoft. Quantum. Canon. repeatc](xref:Microsoft.Quantum.Canon.RepeatC)
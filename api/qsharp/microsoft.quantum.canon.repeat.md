---
uid: Microsoft.Quantum.Canon.Repeat
title: Wiederholungs Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Repeat
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: 5aedd056b851b8d8d7c25a32eb22587292e132a8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703878"
---
# <a name="repeat-operation"></a>Wiederholungs Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Wiederholt einen Vorgang mit einer angegebenen Anzahl von vorkommen.

```qsharp
operation Repeat<'TInput> (op : ('TInput => Unit), nTimes : Int, input : 'TInput) : Unit
```


## <a name="input"></a>Eingabe

### <a name="op--tinput--unit"></a>OP: ' TInput => [Unit](xref:microsoft.quantum.lang-ref.unit) 

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
- [Microsoft. Quantum. Canon. repeata](xref:Microsoft.Quantum.Canon.RepeatA)
- [Microsoft. Quantum. Canon. repeatc](xref:Microsoft.Quantum.Canon.RepeatC)
- [Microsoft. Quantum. Canon. repeatca](xref:Microsoft.Quantum.Canon.RepeatCA)
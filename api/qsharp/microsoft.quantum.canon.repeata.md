---
uid: Microsoft.Quantum.Canon.RepeatA
title: Wiederholungs ATA-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RepeatA
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: 5f418f67d7265d4cb39b3636906c74d33d80f472
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205557"
---
# <a name="repeata-operation"></a>Wiederholungs ATA-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Wiederholt einen Vorgang mit einer angegebenen Anzahl von vorkommen.

```qsharp
operation RepeatA<'TInput> (op : ('TInput => Unit is Adj), nTimes : Int, input : 'TInput) : Unit is Adj
```


## <a name="input"></a>Eingabe

### <a name="op--tinput--unit--is-adj"></a>OP: ' TInput => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ

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
- [Microsoft. Quantum. Canon. repeatc](xref:Microsoft.Quantum.Canon.RepeatC)
- [Microsoft. Quantum. Canon. repeatca](xref:Microsoft.Quantum.Canon.RepeatCA)
---
uid: Microsoft.Quantum.Canon.RepeatA
title: Wiederholungs ATA-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RepeatA
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: 9ae3123a64b2a886df3b7575b2840522f9b011ee
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852221"
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



## <a name="example"></a>Beispiel

Die folgenden sind gleichwertig:

```qsharp
RepeatA(U, 17, target);
(BoundA(ConstantArray(17, U)))(target);
```

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Arrays. drawmany](xref:Microsoft.Quantum.Arrays.DrawMany)
- [Microsoft. Quantum. Canon. Repeat](xref:Microsoft.Quantum.Canon.Repeat)
- [Microsoft. Quantum. Canon. repeatc](xref:Microsoft.Quantum.Canon.RepeatC)
- [Microsoft. Quantum. Canon. repeatca](xref:Microsoft.Quantum.Canon.RepeatCA)
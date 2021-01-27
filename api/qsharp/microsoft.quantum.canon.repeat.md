---
uid: Microsoft.Quantum.Canon.Repeat
title: Wiederholungs Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Repeat
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: 40ee191e8d9044f33aa1621303c70f7e0847e8f6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852243"
---
# <a name="repeat-operation"></a>Wiederholungs Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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



## <a name="example"></a>Beispiel

Die folgenden sind gleichwertig:

```qsharp
Repeat(U, 17, target);
(Bound(ConstantArray(17, U)))(target);
```

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Arrays. drawmany](xref:Microsoft.Quantum.Arrays.DrawMany)
- [Microsoft. Quantum. Canon. repeata](xref:Microsoft.Quantum.Canon.RepeatA)
- [Microsoft. Quantum. Canon. repeatc](xref:Microsoft.Quantum.Canon.RepeatC)
- [Microsoft. Quantum. Canon. repeatca](xref:Microsoft.Quantum.Canon.RepeatCA)
---
uid: Microsoft.Quantum.Arrays.DrawMany
title: Drawmany-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: DrawMany
qsharp.summary: Repeats an operation for a given number of samples, collecting its outputs in an array.
ms.openlocfilehash: 601fe603a869dcf977c1ceade5819ee64f634d53
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706111"
---
# <a name="drawmany-operation"></a>Drawmany-Vorgang

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paketen [](https://nuget.org/packages/)


Wiederholt einen Vorgang für eine bestimmte Anzahl von Samplings und sammelt die Ausgaben in einem Array.

```qsharp
operation DrawMany<'TInput, 'TOutput> (op : ('TInput => 'TOutput), nSamples : Int, input : 'TInput) : 'TOutput[]
```


## <a name="input"></a>Eingabe

### <a name="op--tinput--toutput"></a>OP: ' TInput => ' TOutput 

Der Vorgang, der wiederholt aufgerufen werden soll.


### <a name="nsamples--int"></a>nsamples: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der Samplings zum Aufrufen von `op` zum Erfassen von.


### <a name="input--tinput"></a>Eingabe: ' TInput

Die an zu über gebenden Eingaben `op` .



## <a name="output--toutput"></a>Ausgabe: ' TOutput []



## <a name="type-parameters"></a>Typparameter

### <a name="tinput"></a>' TInput


### <a name="toutput"></a>"TOutput"



## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. Repeat](xref:Microsoft.Quantum.Canon.Repeat)
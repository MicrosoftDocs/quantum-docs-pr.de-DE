---
uid: Microsoft.Quantum.Diagnostics.AllowAtMostNCallsCA
title: Vorgang "zugswatmustncallsca"
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllowAtMostNCallsCA
qsharp.summary: Between a call to this operation and its adjoint, asserts that a given operation is called at most a certain number of times.
ms.openlocfilehash: 7caf33e33318bb74cb160436940eff9f0f2782cc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202565"
---
# <a name="allowatmostncallsca-operation"></a>Vorgang "zugswatmustncallsca"

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Bei einem Aufruf dieses Vorgangs und seines Adjoint-Vorgangs bestätigt, dass ein angegebener Vorgang höchstens eine bestimmte Anzahl von Vorkommen aufgerufen wird.

```qsharp
operation AllowAtMostNCallsCA<'TInput, 'TOutput> (nTimes : Int, op : ('TInput => 'TOutput is Adj + Ctl), message : String) : Unit is Adj
```


## <a name="input"></a>Eingabe

### <a name="ntimes--int"></a>nTimes: [int](xref:microsoft.quantum.lang-ref.int)

Die maximale Anzahl von aufrufen, die `op` aufgerufen werden können.


### <a name="op--tinput--toutput--is-adj--ctl"></a>OP: ' TInput => ' TOutput ist ADJ + CTL

Ein Vorgang, dessen Aufrufe eingeschränkt werden.


### <a name="message--string"></a>Message: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)

Eine Meldung, die bei einem Fehler angezeigt werden soll.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Typparameter

### <a name="tinput"></a>' TInput


### <a name="toutput"></a>"TOutput"



## <a name="remarks"></a>Bemerkungen

Dieser Vorgang kann durch einen No-op-Vorgang für Ziele ersetzt werden, die ihn nicht unterstützen.
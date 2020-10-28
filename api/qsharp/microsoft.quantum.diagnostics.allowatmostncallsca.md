---
uid: Microsoft.Quantum.Diagnostics.AllowAtMostNCallsCA
title: Vorgang "zugswatmustncallsca"
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllowAtMostNCallsCA
qsharp.summary: Between a call to this operation and its adjoint, asserts that a given operation is called at most a certain number of times.
ms.openlocfilehash: 1a9975d2d2026749238430b247cf47738de545cd
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702792"
---
# <a name="allowatmostncallsca-operation"></a>Vorgang "zugswatmustncallsca"

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Paketen [](https://nuget.org/packages/)


Bei einem Aufruf dieses Vorgangs und seines Adjoint-Vorgangs bestätigt, dass ein angegebener Vorgang höchstens eine bestimmte Anzahl von Vorkommen aufgerufen wird.

```qsharp
operation AllowAtMostNCallsCA<'TInput, 'TOutput> (nTimes : Int, op : ('TInput => 'TOutput is Adj + Ctl), message : String) : Unit
```


## <a name="input"></a>Eingabe

### <a name="ntimes--int"></a>nTimes: [int](xref:microsoft.quantum.lang-ref.int)

Die maximale Anzahl von aufrufen, die `op` aufgerufen werden können.


### <a name="op--tinput--toutput-adj--ctl"></a>OP: ' TInput => ' TOutput ADJ + CTL

Ein Vorgang, dessen Aufrufe eingeschränkt werden.


### <a name="message--string"></a>Message: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)

Eine Meldung, die bei einem Fehler angezeigt werden soll.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Typparameter

### <a name="tinput"></a>' TInput


### <a name="toutput"></a>"TOutput"



## <a name="remarks"></a>Hinweise

Dieser Vorgang kann durch einen No-op-Vorgang für Ziele ersetzt werden, die ihn nicht unterstützen.
---
uid: Microsoft.Quantum.Diagnostics.AllowAtMostNCallsCA
title: Vorgang "zugswatmustncallsca"
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllowAtMostNCallsCA
qsharp.summary: Between a call to this operation and its adjoint, asserts that a given operation is called at most a certain number of times.
ms.openlocfilehash: bb6ba2615b571b0d9d056b93f8e36d2dec0c4a21
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853533"
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



## <a name="example"></a>Beispiel

Der folgende Code Ausschnitt schlägt fehl, wenn er auf Computern ausgeführt wird, die diese Diagnose unterstützen:

```qsharp
using (register = Qubit[4]) {
    within {
        AllowAtMostNCallsCA(3, H, "Too many calls to H.");
    } apply {
        // Fails since this calls H four times, rather than the
        // allowed maximum of three.
        ApplyToEach(H, register);
    }
}
```

## <a name="remarks"></a>Bemerkungen

Dieser Vorgang kann durch einen No-op-Vorgang für Ziele ersetzt werden, die ihn nicht unterstützen.
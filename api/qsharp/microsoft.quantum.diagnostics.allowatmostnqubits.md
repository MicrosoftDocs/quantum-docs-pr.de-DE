---
uid: Microsoft.Quantum.Diagnostics.AllowAtMostNQubits
title: Vorgang "Zuordnung"
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllowAtMostNQubits
qsharp.summary: Between a call to this operation and its adjoint, asserts that at most a given number of additional qubits are allocated with using statements.
ms.openlocfilehash: ddbed96df0d95cfd78730c091a6a81ee6e49c349
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702791"
---
# <a name="allowatmostnqubits-operation"></a>Vorgang "Zuordnung"

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Paketen [](https://nuget.org/packages/)


Bei einem Aufrufe dieses Vorgangs und seines Adjoint-Vorgangs wird von bestätigt, dass höchstens eine angegebene Anzahl zusätzlicher Qubits mit using-Anweisungen zugeordnet wird.

```qsharp
operation AllowAtMostNQubits (nQubits : Int, message : String) : Unit
```


## <a name="input"></a>Eingabe

### <a name="nqubits--int"></a>nqubits: [int](xref:microsoft.quantum.lang-ref.int)

Die maximale Anzahl von Qubits, die zugeordnet werden können.


### <a name="message--string"></a>Message: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)

Eine Meldung, die bei einem Fehler angezeigt werden soll.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Hinweise

Dieser Vorgang kann durch einen No-op-Vorgang für Ziele ersetzt werden, die ihn nicht unterstützen.
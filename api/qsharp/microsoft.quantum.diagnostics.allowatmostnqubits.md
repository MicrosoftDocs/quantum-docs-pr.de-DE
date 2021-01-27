---
uid: Microsoft.Quantum.Diagnostics.AllowAtMostNQubits
title: Vorgang "Zuordnung"
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllowAtMostNQubits
qsharp.summary: Between a call to this operation and its adjoint, asserts that at most a given number of additional qubits are allocated with using statements.
ms.openlocfilehash: 3aa80767ac0f752e7be0efa2966c580ca3cb8f19
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98830916"
---
# <a name="allowatmostnqubits-operation"></a>Vorgang "Zuordnung"

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Bei einem Aufrufe dieses Vorgangs und seines Adjoint-Vorgangs wird von bestätigt, dass höchstens eine angegebene Anzahl zusätzlicher Qubits mit using-Anweisungen zugeordnet wird.

```qsharp
operation AllowAtMostNQubits (nQubits : Int, message : String) : Unit is Adj
```


## <a name="input"></a>Eingabe

### <a name="nqubits--int"></a>nqubits: [int](xref:microsoft.quantum.lang-ref.int)

Die maximale Anzahl von Qubits, die zugeordnet werden können.


### <a name="message--string"></a>Message: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)

Eine Meldung, die bei einem Fehler angezeigt werden soll.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="example"></a>Beispiel

Der folgende Code Ausschnitt schlägt fehl, wenn er auf Computern ausgeführt wird, die diese Diagnose unterstützen:

```qsharp
within {
    AllowAtMostNQubits(3, "Too many qubits allocated.");
} apply {
    // Fails since this allocates four qubits.
    using (register = Qubit[4]) {
    }
}
```

## <a name="remarks"></a>Bemerkungen

Dieser Vorgang kann durch einen No-op-Vorgang für Ziele ersetzt werden, die ihn nicht unterstützen.
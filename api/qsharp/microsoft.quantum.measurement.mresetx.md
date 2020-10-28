---
uid: Microsoft.Quantum.Measurement.MResetX
title: Mresetx-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MResetX
qsharp.summary: Measures a single qubit in the X basis, and resets it to a fixed initial state following the measurement.
ms.openlocfilehash: a16d7405388b560edcdb6c36b6668791f7ba1398
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725005"
---
# <a name="mresetx-operation"></a>Mresetx-Vorgang

Namespace: [Microsoft. Quantum. Measurement](xref:Microsoft.Quantum.Measurement)

Paketen [](https://nuget.org/packages/)


Misst ein einzelnes Qubit in der X-Basis und setzt es nach der Messung auf einen festgelegten Anfangszustand zurück.

```qsharp
operation MResetX (target : Qubit) : Result
```


## <a name="description"></a>BESCHREIBUNG

Führt eine einzelne Qubit-Messung im $X $-Basis aus und stellt sicher, dass das Qubit nach der Messung an $ \ket $ zurückgegeben wird {0} .

## <a name="input"></a>Eingabe

### <a name="target--qubit"></a>Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Ein einzelnes Qubit, das gemessen werden soll.



## <a name="output--__invalidresult__"></a>Ausgabe: __ungültig <Result>__

Das Ergebnis der Messung `target` im Pauli-$X $.
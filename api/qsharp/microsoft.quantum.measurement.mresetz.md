---
uid: Microsoft.Quantum.Measurement.MResetZ
title: Mresetz-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MResetZ
qsharp.summary: Measures a single qubit in the Z basis, and resets it to a fixed initial state following the measurement.
ms.openlocfilehash: fc9ba6576b56d7df1a57334e1da46b9c48376ecb
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853743"
---
# <a name="mresetz-operation"></a>Mresetz-Vorgang

Namespace: [Microsoft. Quantum. Measurement](xref:Microsoft.Quantum.Measurement)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Misst ein einzelnes Qubit in der Z-Basis und setzt es nach der Messung auf einen festgelegten Anfangszustand zurück.

```qsharp
operation MResetZ (target : Qubit) : Result
```


## <a name="description"></a>Beschreibung

Führt eine einzelne Qubit-Messung im $Z $-Basis aus und stellt sicher, dass das Qubit nach der Messung an $ \ket $ zurückgegeben wird {0} .

## <a name="input"></a>Eingabe

### <a name="target--qubit"></a>Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Ein einzelnes Qubit, das gemessen werden soll.



## <a name="output--__invalidresult__"></a>Ausgabe: __ungültig <Result>__

Das Ergebnis der Messung `target` im Pauli-$Z $.
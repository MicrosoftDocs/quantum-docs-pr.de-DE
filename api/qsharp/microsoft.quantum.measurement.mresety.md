---
uid: Microsoft.Quantum.Measurement.MResetY
title: Mresegty-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MResetY
qsharp.summary: Measures a single qubit in the Y basis, and resets it to a fixed initial state following the measurement.
ms.openlocfilehash: 2e41e76a46b68178a8a22b39131d6ca2a8c50b64
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854637"
---
# <a name="mresety-operation"></a>Mresegty-Vorgang

Namespace: [Microsoft. Quantum. Measurement](xref:Microsoft.Quantum.Measurement)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Misst ein einzelnes Qubit in der Y-Basis und setzt es nach der Messung auf einen festgelegten Anfangszustand zurück.

```qsharp
operation MResetY (target : Qubit) : Result
```


## <a name="description"></a>Beschreibung

Führt eine einzelne Qubit-Messung im $Y $-Basis aus und stellt sicher, dass das Qubit nach der Messung an $ \ket $ zurückgegeben wird {0} .

## <a name="input"></a>Eingabe

### <a name="target--qubit"></a>Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Ein einzelnes Qubit, das gemessen werden soll.



## <a name="output--__invalidresult__"></a>Ausgabe: __ungültig <Result>__

Das Ergebnis der Messung `target` im Pauli-$Y $.
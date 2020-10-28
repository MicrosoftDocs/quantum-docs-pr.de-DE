---
uid: Microsoft.Quantum.Measurement.MResetY
title: Mresegty-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MResetY
qsharp.summary: Measures a single qubit in the Y basis, and resets it to a fixed initial state following the measurement.
ms.openlocfilehash: 48aba7317d0e48d089ec6c4814efdee51bb8e2ed
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725006"
---
# <a name="mresety-operation"></a>Mresegty-Vorgang

Namespace: [Microsoft. Quantum. Measurement](xref:Microsoft.Quantum.Measurement)

Paketen [](https://nuget.org/packages/)


Misst ein einzelnes Qubit in der Y-Basis und setzt es nach der Messung auf einen festgelegten Anfangszustand zurück.

```qsharp
operation MResetY (target : Qubit) : Result
```


## <a name="description"></a>BESCHREIBUNG

Führt eine einzelne Qubit-Messung im $Y $-Basis aus und stellt sicher, dass das Qubit nach der Messung an $ \ket $ zurückgegeben wird {0} .

## <a name="input"></a>Eingabe

### <a name="target--qubit"></a>Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Ein einzelnes Qubit, das gemessen werden soll.



## <a name="output--__invalidresult__"></a>Ausgabe: __ungültig <Result>__

Das Ergebnis der Messung `target` im Pauli-$Y $.
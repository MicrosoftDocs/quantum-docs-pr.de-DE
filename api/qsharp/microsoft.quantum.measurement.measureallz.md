---
uid: Microsoft.Quantum.Measurement.MeasureAllZ
title: -Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasureAllZ
qsharp.summary: Jointly measures a register of qubits in the Pauli Z basis.
ms.openlocfilehash: cb3c7cab33efb612bbf5da3b51d2df5d1b8ba1df
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854671"
---
# <a name="measureallz-operation"></a>-Vorgang

Namespace: [Microsoft. Quantum. Measurement](xref:Microsoft.Quantum.Measurement)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Misst gemeinsam ein Register von Qubits in der Pauli Z-Basis.

```qsharp
operation MeasureAllZ (register : Qubit[]) : Result
```


## <a name="description"></a>Beschreibung

Misst ein Register von Qubits im $Z \otimes z \otimes \cdots \otimes z $, das die Parität des gesamten Registers darstellt.

## <a name="input"></a>Eingabe

### <a name="register--qubit"></a>Register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Das zu messende Register.



## <a name="output--__invalidresult__"></a>Ausgabe: __ungültig <Result>__

Das Ergebnis der Messung $Z \otimes z \otimes \cdots \otimes z $.
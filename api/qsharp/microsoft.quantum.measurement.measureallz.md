---
uid: Microsoft.Quantum.Measurement.MeasureAllZ
title: -Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasureAllZ
qsharp.summary: Jointly measures a register of qubits in the Pauli Z basis.
ms.openlocfilehash: 6c44ab6a7983697644071f0e3cf106e9825661ee
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96227079"
---
# <a name="measureallz-operation"></a>-Vorgang

Namespace: [Microsoft. Quantum. Measurement](xref:Microsoft.Quantum.Measurement)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Misst gemeinsam ein Register von Qubits in der Pauli Z-Basis.

```qsharp
operation MeasureAllZ (register : Qubit[]) : Result
```


## <a name="description"></a>BESCHREIBUNG

Misst ein Register von Qubits im $Z \otimes z \otimes \cdots \otimes z $, das die Parität des gesamten Registers darstellt.

## <a name="input"></a>Eingabe

### <a name="register--qubit"></a>Register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Das zu messende Register.



## <a name="output--__invalidresult__"></a>Ausgabe: __ungültig <Result>__

Das Ergebnis der Messung $Z \otimes z \otimes \cdots \otimes z $.
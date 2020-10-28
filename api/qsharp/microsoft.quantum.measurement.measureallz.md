---
uid: Microsoft.Quantum.Measurement.MeasureAllZ
title: -Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasureAllZ
qsharp.summary: Jointly measures a register of qubits in the Pauli Z basis.
ms.openlocfilehash: 4ac36a77b37f672859e61f3db89a43f4ca1fc93c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701940"
---
# <a name="measureallz-operation"></a>-Vorgang

Namespace: [Microsoft. Quantum. Measurement](xref:Microsoft.Quantum.Measurement)

Paketen [](https://nuget.org/packages/)


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
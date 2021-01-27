---
uid: Microsoft.Quantum.Measurement.MeasureWithScratch
title: Erstellungs Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MeasureWithScratch
qsharp.summary: Measures the given Pauli operator using an explicit scratch qubit to perform the measurement.
ms.openlocfilehash: 4173aa9daac08a3febdfcbf12dc236f797685436
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854658"
---
# <a name="measurewithscratch-operation"></a>Erstellungs Vorgang

Namespace: [Microsoft. Quantum. Measurement](xref:Microsoft.Quantum.Measurement)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Misst den angegebenen Pauli-Operator mithilfe eines expliziten Scratch-Qubit, um die Messung auszuführen.

```qsharp
operation MeasureWithScratch (pauli : Pauli[], target : Qubit[]) : Result
```


## <a name="input"></a>Eingabe

### <a name="pauli--pauli"></a>Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]

Ein Multi-Qubit-Pauli-Operator, der als Array von Single-Qubit-Pauli-Operatoren angegeben wird.


### <a name="target--qubit"></a>Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Die zu messende Qubit-Registrierung.



## <a name="output--__invalidresult__"></a>Ausgabe: __ungültig <Result>__

Das Ergebnis der Messung des angegebenen Pauli-Operators für das `target` Register.
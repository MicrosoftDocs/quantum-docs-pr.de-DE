---
uid: Microsoft.Quantum.Diagnostics.AssertMeasurement
title: Assertmeasurement-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertMeasurement
qsharp.summary: Asserts that measuring the given qubits in the given Pauli basis will always have the given result.
ms.openlocfilehash: 09024cd8cd6e713360dcf7f42f55941590f35883
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702780"
---
# <a name="assertmeasurement-operation"></a>Assertmeasurement-Vorgang

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Paketen [](https://nuget.org/packages/)


Bestätigt, dass das Messen der angegebenen Qubits in der angegebenen Pauli-Basis immer das angegebene Ergebnis hat.

```qsharp
operation AssertMeasurement (bases : Pauli[], qubits : Qubit[], result : Result, msg : String) : Unit
```


## <a name="input"></a>Eingabe

### <a name="bases--pauli"></a>Basen: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]

Ein Maßeffekt zur Bestätigung der Wahrscheinlichkeit von, ausgedrückt als Multi-Qubit-Pauli-Operator.


### <a name="qubits--qubit"></a>Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Ein Register, für das die-Assertion durchführen werden soll.


### <a name="result--__invalidresult__"></a>Ergebnis: __ungültig <Result>__

Das erwartete Ergebnis von `Measure(bases, qubits)` .


### <a name="msg--string"></a>msg: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)

Eine Meldung, die gemeldet werden soll, wenn die Übersetzung fehlschlägt.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Hinweise

Beachten Sie, dass die unter-und kontrollierten Versionen dieses Vorgangs die Bedingung nicht überprüfen.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Diagnostics. assertmessrementwahrscheinlichkeits](xref:Microsoft.Quantum.Diagnostics.AssertMeasurementProbability)
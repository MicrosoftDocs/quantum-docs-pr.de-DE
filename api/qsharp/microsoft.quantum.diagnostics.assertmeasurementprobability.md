---
uid: Microsoft.Quantum.Diagnostics.AssertMeasurementProbability
title: Assertmessrementwahrscheinlichkeits-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertMeasurementProbability
qsharp.summary: Asserts that measuring the given qubits in the given Pauli basis will have the given result with the given probability, within some tolerance.
ms.openlocfilehash: ff0419706d825442492f82e564f1cce86f1b112f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702756"
---
# <a name="assertmeasurementprobability-operation"></a>Assertmessrementwahrscheinlichkeits-Vorgang

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Paketen [](https://nuget.org/packages/)


Bestätigt, dass das Messen der angegebenen Qubits in der angegebenen Pauli-Basis das angegebene Ergebnis mit der angegebenen Wahrscheinlichkeit innerhalb einiger Toleranz hat.

```qsharp
operation AssertMeasurementProbability (bases : Pauli[], qubits : Qubit[], result : Result, prob : Double, msg : String, tol : Double) : Unit
```


## <a name="input"></a>Eingabe

### <a name="bases--pauli"></a>Basen: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]

Ein Maßeffekt zur Bestätigung der Wahrscheinlichkeit von, ausgedrückt als Multi-Qubit-Pauli-Operator.


### <a name="qubits--qubit"></a>Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Ein Register, für das die-Assertion durchführen werden soll.


### <a name="result--__invalidresult__"></a>Ergebnis: __ungültig <Result>__

Erwartetes Ergebnis von `Measure(bases, qubits)` .


### <a name="prob--double"></a>prob: [Double](xref:microsoft.quantum.lang-ref.double)

Die Wahrscheinlichkeit, mit der das angegebene Ergebnis erwartet wird.


### <a name="msg--string"></a>msg: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)

Eine Meldung, die gemeldet werden soll, wenn die Übersetzung fehlschlägt.


### <a name="tol--double"></a>Tol: [Double](xref:microsoft.quantum.lang-ref.double)





## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Hinweise

Beachten Sie, dass die unter-und kontrollierten Versionen dieses Vorgangs die Bedingung nicht überprüfen.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Diagnostics. assertmeasurement](xref:Microsoft.Quantum.Diagnostics.AssertMeasurement)
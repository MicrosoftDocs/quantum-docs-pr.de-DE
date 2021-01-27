---
uid: Microsoft.Quantum.Diagnostics.AssertMeasurementProbability
title: Assertmessrementwahrscheinlichkeits-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertMeasurementProbability
qsharp.summary: Asserts that measuring the given qubits in the given Pauli basis will have the given result with the given probability, within some tolerance.
ms.openlocfilehash: 2fd89121516ef6994dedb75b214589b4e360ff8b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98830821"
---
# <a name="assertmeasurementprobability-operation"></a>Assertmessrementwahrscheinlichkeits-Vorgang

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Bestätigt, dass das Messen der angegebenen Qubits in der angegebenen Pauli-Basis das angegebene Ergebnis mit der angegebenen Wahrscheinlichkeit innerhalb einiger Toleranz hat.

```qsharp
operation AssertMeasurementProbability (bases : Pauli[], qubits : Qubit[], result : Result, prob : Double, msg : String, tol : Double) : Unit is Adj + Ctl
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



## <a name="example"></a>Beispiel

```qsharp
using (register = Qubit()) {
    H(register);
    AssertProb([PauliZ], [register], One, 0.5,
        "Measuring in conjugate basis did not give 50/50 results.", 1e-5);
}
```

## <a name="remarks"></a>Bemerkungen

Beachten Sie, dass die unter-und kontrollierten Versionen dieses Vorgangs die Bedingung nicht überprüfen.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Diagnostics. assertmeasurement](xref:Microsoft.Quantum.Diagnostics.AssertMeasurement)
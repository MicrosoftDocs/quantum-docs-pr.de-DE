---
uid: Microsoft.Quantum.Arithmetic.AssertProbInt
title: Assertprobint-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertProbInt
qsharp.summary: Asserts that the probability of a specific state of a quantum register has the expected value.
ms.openlocfilehash: a8e4217e18528adc0aa9923f1c0dcfb59e1d2488
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707439"
---
# <a name="assertprobint-operation"></a>Assertprobint-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paketen [](https://nuget.org/packages/)


Bestätigt, dass die Wahrscheinlichkeit eines bestimmten Zustands eines Quantum-Register über den erwarteten Wert verfügt.

```qsharp
operation AssertProbInt (stateIndex : Int, expected : Double, qubits : Microsoft.Quantum.Arithmetic.LittleEndian, tolerance : Double) : Unit
```


## <a name="description"></a>BESCHREIBUNG

Bestätigt bei einem $n $-Qubit-Quantum-Status $ \ket{\psi} = \sum ^ {2 ^ n-1} _ {j = 0} \ alpha_j \ket{j} $, dass die Wahrscheinlichkeit $ | \ alpha_j | ^ 2 $ des durch $j $ indizierten Zustands $ \ket{j} $ den erwarteten Wert hat.

## <a name="input"></a>Eingabe

### <a name="stateindex--int"></a>Status Index: [int](xref:microsoft.quantum.lang-ref.int)

Der Index $j $ des Zustands $ \ket{j} $, der durch ein `LittleEndian` Register dargestellt wird.


### <a name="expected--double"></a>erwartet: [Double](xref:microsoft.quantum.lang-ref.double)

Der erwartete Wert von $ | \ alpha_j | ^ 2 $.


### <a name="qubits--littleendian"></a>Qubits: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Das Qubit-Register, das $ \ket{\psi} $ im Little-Endian-Format speichert.


### <a name="tolerance--double"></a>Toleranz: [Double](xref:microsoft.quantum.lang-ref.double)

Absolute Toleranz für den Unterschied zwischen tatsächlichem und erwartetem Verhalten.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)


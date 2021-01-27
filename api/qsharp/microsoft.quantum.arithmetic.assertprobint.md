---
uid: Microsoft.Quantum.Arithmetic.AssertProbInt
title: Assertprobint-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertProbInt
qsharp.summary: Asserts that the probability of a specific state of a quantum register has the expected value.
ms.openlocfilehash: 85ff04bbad9dc2ed0f803db65508fdfbb0d22c56
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843404"
---
# <a name="assertprobint-operation"></a>Assertprobint-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Bestätigt, dass die Wahrscheinlichkeit eines bestimmten Zustands eines Quantum-Register über den erwarteten Wert verfügt.

```qsharp
operation AssertProbInt (stateIndex : Int, expected : Double, qubits : Microsoft.Quantum.Arithmetic.LittleEndian, tolerance : Double) : Unit
```


## <a name="description"></a>Beschreibung

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



## <a name="example"></a>Beispiel

Angenommen, das `qubits` Register codiert einen 3-Qubit-Quantum-Status $ \ket{\psi} = \ sqrt {1/8} \ Ket {0} + \ sqrt {7/8} \ Ket {6} $ im Little-Endian-Format.
Dies bedeutet, dass die Zahl "$ \ket {0} \equiv\ket {0} \ket {0} \ket {0} $" und "$ \ket {6} \equiv\ket {0} \ket {1} \ket {1} $" lautet. Die folgenden Bestätigungen werden erfolgreich ausgeführt:

```qsharp
AssertProbInt(0, 0.125, qubits, 10e-10);
AssertProbInt(6, 0.875, qubits, 10e-10);
```
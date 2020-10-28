---
uid: Microsoft.Quantum.Canon.MultiplexZ
title: Multiplexz-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexZ
qsharp.summary: Applies a Pauli Z rotation conditioned on an array of qubits.
ms.openlocfilehash: f7b1973e18ad396ebe892ad63ae47374a7cafbd5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703956"
---
# <a name="multiplexz-operation"></a>Multiplexz-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Wendet eine Pauli Z-Drehung an, die auf ein Array von Qubits bedingt ist.

```qsharp
operation MultiplexZ (coefficients : Double[], control : Microsoft.Quantum.Arithmetic.LittleEndian, target : Qubit) : Unit
```


## <a name="description"></a>BESCHREIBUNG

Dadurch wird der Multiplikations gesteuerte einheitliche Vorgang angewendet, der die Drehung durch den Winkel $ \ theta_j $ um einen Single-Qubit-Pauli-Operator $Z $ durchführt, wenn er vom $n $-Qubit-Zahlen Status $ \ket{j} $ gesteuert wird.
Insbesondere kann dieser Vorgang durch die einheitliche

$ $ \begin{align} U = \sum ^ {2 ^ n-1} _ {j = 0} \ket{j}\bra{j} \otimes e ^ {i Z \ theta_j}.
\end{align} $ $

## <a name="input"></a>Eingabe

### <a name="coefficients--double"></a>Koeffizienten: [Double](xref:microsoft.quantum.lang-ref.double)[]

Array von bis zu $2 ^ n $ Koeffizienten $ \ theta_j $. Der $j $ Th-Koeffizienten indiziert den im Little-Endian-Format codierten Zahlen Status $ \ket{j} $.


### <a name="control--littleendian"></a>Control: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$n $-Qubit-Steuerelement Register, das die Anzahl der Zustände $ \ket{j} $ im Little-Endian-Format codiert.


### <a name="target--qubit"></a>Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Einzelnes Qubit-Register, das durch $e ^ {i P \ theta_j} $ gedreht wird.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Hinweise

`coefficients` wird mit Elementen $ \ theta_j = $0,0 aufgefüllt, wenn weniger als $2 ^ n $ angegeben werden.

## <a name="references"></a>Referenzen

- Synthese von Quantum Logic-Leitungen Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. ungefähre atelymultiplexz](xref:Microsoft.Quantum.Canon.ApproximatelyMultiplexZ)
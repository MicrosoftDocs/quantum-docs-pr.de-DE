---
uid: Microsoft.Quantum.Canon.MultiplexPauli
title: Multiplexpauli-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexPauli
qsharp.summary: Applies a Pauli rotation conditioned on an array of qubits.
ms.openlocfilehash: 0714e796c1e5ad097814bcf507f49f59a844e9ff
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703961"
---
# <a name="multiplexpauli-operation"></a>Multiplexpauli-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Wendet eine für ein Array von Qubits bedingte Pauli-Rotation an.

```qsharp
operation MultiplexPauli (coefficients : Double[], pauli : Pauli, control : Microsoft.Quantum.Arithmetic.LittleEndian, target : Qubit) : Unit
```


## <a name="description"></a>BESCHREIBUNG

Dadurch wird ein mehrfach gesteuerter einheitlicher Vorgang angewendet, bei dem die Drehung um den Winkel $ \ theta_j $ um einen Single-Qubit-Pauli-Operator $P $ durchführt, wenn er vom $n $-Qubit-Zahlen Status $ \ket{j} $ gesteuert wird.
Insbesondere wird die Aktion dieses Vorgangs durch die einheitliche

$ $ \begin{align} U = \sum ^ {2 ^ n-1} _ {j = 0} \ket{j}\bra{j} \otimes e ^ {i P \ theta_j}.
\end{align} $ $

## <a name="input"></a>Eingabe

### <a name="coefficients--double"></a>Koeffizienten: [Double](xref:microsoft.quantum.lang-ref.double)[]

Array von bis zu $2 ^ n $ Koeffizienten $ \ theta_j $. Der $j $ Th-Koeffizienten indiziert den im Little-Endian-Format codierten Zahlen Status $ \ket{j} $.


### <a name="pauli--pauli"></a>Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

Der Pauli-Operator $P $, der die Achse der Drehung bestimmt.


### <a name="control--littleendian"></a>Control: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$n $-Qubit-Steuerelement Register, das die Anzahl der Zustände $ \ket{j} $ im Little-Endian-Format codiert.


### <a name="target--qubit"></a>Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Einzelnes Qubit-Register, das durch $e ^ {i P \ theta_j} $ gedreht wird.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Hinweise

`coefficients` wird mit Elementen $ \ theta_j = $0,0 aufgefüllt, wenn weniger als $2 ^ n $ angegeben werden.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. näherymultiplexpauli](xref:Microsoft.Quantum.Canon.ApproximatelyMultiplexPauli)
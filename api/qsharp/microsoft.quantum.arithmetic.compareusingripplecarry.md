---
uid: Microsoft.Quantum.Arithmetic.CompareUsingRippleCarry
title: Compareusingripplecarry-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareUsingRippleCarry
qsharp.summary: This operation tests if an integer represented by a register of qubits is greater than another integer, applying an XOR of the result onto an output qubit.
ms.openlocfilehash: e2d6e5a663f8c4e101c7e2ab1346d10cade3f4e0
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223458"
---
# <a name="compareusingripplecarry-operation"></a>Compareusingripplecarry-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Dieser Vorgang testet, ob eine ganze Zahl, die durch ein Register von Qubits dargestellt wird, größer als eine andere Ganzzahl ist, und wendet ein XOR des Ergebnisses auf ein Ausgabe-Qubit an.

```qsharp
operation CompareUsingRippleCarry (x : Microsoft.Quantum.Arithmetic.LittleEndian, y : Microsoft.Quantum.Arithmetic.LittleEndian, output : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a>BESCHREIBUNG

Bei zwei Ganzzahlen `x` `y` , die in gleich großen Qubit-Registern gespeichert sind, überprüft dieser Vorgang, ob Sie übereinstimmen `x > y` . True gibt an, dass 1 ein XoReD in ein Ausgabe-Qubit ist. Andernfalls wird 0 in einem Ausgabe-Qubit als XoReD fest.
Mit anderen Worten: dieser Vorgang kann durch die einheitliche $ $ \begin{align} u\ket {x} \ Ket {y} \ Ket {z} = \ket{x}\ket{y}\ket{z\oplus (x>y)} dargestellt werden.
\end{align} $ $

## <a name="input"></a>Eingabe

### <a name="x--littleendian"></a>x: [littleandian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Die erste zu vergleichende Zahl, die im `LittleEndian` Format in einem Qubit-Register gespeichert wird.


### <a name="y--littleendian"></a>y: [littleddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Die zweite zu vergleichende Zahl, die im `LittleEndian` Format in einem Qubit-Register gespeichert werden soll.


### <a name="output--qubit"></a>Ausgabe: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Ein Qubit, das das Ergebnis des Vergleichs $x>y $ speichert.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>Referenzen

- Eine neue Quantum Ripple-be Additions Verbindung Steven a. Cuccaro, Thomas G. Draper, Samuel A. KUTIN, David Petrie Moulton https://arxiv.org/abs/quant-ph/0410184
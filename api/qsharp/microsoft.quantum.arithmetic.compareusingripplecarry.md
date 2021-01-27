---
uid: Microsoft.Quantum.Arithmetic.CompareUsingRippleCarry
title: Compareusingripplecarry-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareUsingRippleCarry
qsharp.summary: This operation tests if an integer represented by a register of qubits is greater than another integer, applying an XOR of the result onto an output qubit.
ms.openlocfilehash: ce2be140ecfed21dea6212651249b4a11d2542c8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843291"
---
# <a name="compareusingripplecarry-operation"></a>Compareusingripplecarry-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Dieser Vorgang testet, ob eine ganze Zahl, die durch ein Register von Qubits dargestellt wird, größer als eine andere Ganzzahl ist, und wendet ein XOR des Ergebnisses auf ein Ausgabe-Qubit an.

```qsharp
operation CompareUsingRippleCarry (x : Microsoft.Quantum.Arithmetic.LittleEndian, y : Microsoft.Quantum.Arithmetic.LittleEndian, output : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a>Beschreibung

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



## <a name="references"></a>References

- Eine neue Quantum Ripple-be Additions Verbindung Steven a. Cuccaro, Thomas G. Draper, Samuel A. KUTIN, David Petrie Moulton https://arxiv.org/abs/quant-ph/0410184
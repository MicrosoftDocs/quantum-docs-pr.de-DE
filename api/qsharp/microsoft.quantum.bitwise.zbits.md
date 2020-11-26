---
uid: Microsoft.Quantum.Bitwise.ZBits
title: Zbits-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: ZBits
qsharp.summary: Returns an integer representing the Z bits of an array of Pauli operators.
ms.openlocfilehash: 3ded981dc53236a48f1fb8f6ae12e39c17469447
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219446"
---
# <a name="zbits-function"></a>Zbits-Funktion

Namespace: [Microsoft. Quantum. bitse](xref:Microsoft.Quantum.Bitwise)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Gibt eine ganze Zahl zurück, die die Z-Bits eines Arrays von Pauli-Operatoren darstellt.

```qsharp
function ZBits (paulis : Pauli[]) : Int
```


## <a name="input"></a>Eingabe

### <a name="paulis--pauli"></a>Paulis: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]

Ein Array von Pauli-Operatoren, das als ganze Zahl dargestellt werden soll.



## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)

Eine ganze Zahl $x $ mit binärer Darstellung $ (P_ {62} \, P_ {61} \, \dots \, p_0) $, wobei $p _I = $0, wenn gleich `paulis[i]` `PauliI` oder ist `PauliX` und wobei $p _I = $1 ist, wenn `paulis[i]` `PauliY` oder ist `PauliZ` .

## <a name="remarks"></a>Bemerkungen

Die Funktion löst aus, wenn die Länge des `paulis` Arrays größer als 63 ist.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. bitse. xbits](xref:Microsoft.Quantum.Bitwise.XBits)
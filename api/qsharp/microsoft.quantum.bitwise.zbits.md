---
uid: Microsoft.Quantum.Bitwise.ZBits
title: Zbits-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: ZBits
qsharp.summary: Returns an integer representing the Z bits of an array of Pauli operators.
ms.openlocfilehash: f66b8ef0370e898dd1d095ff2840c91566f32cb8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705551"
---
# <a name="zbits-function"></a>Zbits-Funktion

Namespace: [Microsoft. Quantum. bitse](xref:Microsoft.Quantum.Bitwise)

Paketen [](https://nuget.org/packages/)


Gibt eine ganze Zahl zurück, die die Z-Bits eines Arrays von Pauli-Operatoren darstellt.

```qsharp
function ZBits (paulis : Pauli[]) : Int
```


## <a name="input"></a>Eingabe

### <a name="paulis--pauli"></a>Paulis: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]

Ein Array von Pauli-Operatoren, das als ganze Zahl dargestellt werden soll.



## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)

Eine ganze Zahl $x $ mit binärer Darstellung $ (P_ {62} \, P_ {61} \, \dots \, p_0) $, wobei $p _I = $0, wenn gleich `paulis[i]` `PauliI` oder ist `PauliX` und wobei $p _I = $1 ist, wenn `paulis[i]` `PauliY` oder ist `PauliZ` .

## <a name="remarks"></a>Hinweise

Die Funktion löst aus, wenn die Länge des `paulis` Arrays größer als 63 ist.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. bitse. xbits](xref:Microsoft.Quantum.Bitwise.XBits)
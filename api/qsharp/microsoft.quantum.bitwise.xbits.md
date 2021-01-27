---
uid: Microsoft.Quantum.Bitwise.XBits
title: Xbits-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: XBits
qsharp.summary: Returns an integer representing the X bits of an array of Pauli operators.
ms.openlocfilehash: ddaace8df6e4c47c4affe2eeffb8d8ce31f37327
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845247"
---
# <a name="xbits-function"></a>Xbits-Funktion

Namespace: [Microsoft. Quantum. bitse](xref:Microsoft.Quantum.Bitwise)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Gibt eine ganze Zahl zurück, die die X-Bits eines Arrays von Pauli-Operatoren darstellt.

```qsharp
function XBits (paulis : Pauli[]) : Int
```


## <a name="input"></a>Eingabe

### <a name="paulis--pauli"></a>Paulis: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]

Ein Array von Pauli-Operatoren, das als ganze Zahl dargestellt werden soll.



## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)

Eine ganze Zahl $x $ mit binärer Darstellung $ (P_ {62} \, P_ {61} \, \dots \, p_0) $, wobei $p _I = $0, wenn gleich `paulis[i]` `PauliI` oder ist `PauliZ` und wobei $p _I = $1 ist, wenn `paulis[i]` `PauliX` oder ist `PauliY` .

## <a name="remarks"></a>Bemerkungen

Die Funktion löst aus, wenn die Länge des `paulis` Arrays größer als 63 ist.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. bitse. zbits](xref:Microsoft.Quantum.Bitwise.ZBits)
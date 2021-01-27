---
uid: Microsoft.Quantum.Convert.IntAsBoolArray
title: Intasboolarray-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: IntAsBoolArray
qsharp.summary: Produces a binary representation of a non-negative integer, using the little-endian representation for the returned array.
ms.openlocfilehash: 8b3d230605cc756a5da01e45e47f91c5b8e9f541
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98833306"
---
# <a name="intasboolarray-function"></a>Intasboolarray-Funktion

Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Erzeugt eine binäre Darstellung einer nicht negativen ganzen Zahl unter Verwendung der Little-dendian-Darstellung für das zurückgegebene Array.

```qsharp
function IntAsBoolArray (number : Int, bits : Int) : Bool[]
```


## <a name="input"></a>Eingabe

### <a name="number--int"></a>Zahl: [int](xref:microsoft.quantum.lang-ref.int)

Eine nicht negative ganze Zahl, die in ein Array von booleschen Werten konvertiert werden soll.


### <a name="bits--int"></a>Bits: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der Bits in der binären Darstellung von `number` .



## <a name="output--bool"></a>Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)[]

Ein Array von booleschen Werten, die darstellen `number` .

## <a name="remarks"></a>Bemerkungen

Die Eingabe `bits` muss zwischen 0 und 63 liegen.
Die Eingabe `number` muss zwischen 0 und $2 ^ {\texttt{Bits}}-$1 liegen.
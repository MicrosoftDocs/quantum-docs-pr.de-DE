---
uid: Microsoft.Quantum.Convert.IntAsBoolArray
title: Intasboolarray-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: IntAsBoolArray
qsharp.summary: Produces a binary representation of a positive integer, using the little-endian representation for the returned array.
ms.openlocfilehash: f89cb3d7ca29d7deaaf49573b2670534166caded
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224342"
---
# <a name="intasboolarray-function"></a>Intasboolarray-Funktion

Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Erzeugt eine binäre Darstellung einer positiven ganzen Zahl unter Verwendung der Little-dendian-Darstellung für das zurückgegebene Array.

```qsharp
function IntAsBoolArray (number : Int, bits : Int) : Bool[]
```


## <a name="input"></a>Eingabe

### <a name="number--int"></a>Zahl: [int](xref:microsoft.quantum.lang-ref.int)

Eine positive ganze Zahl, die in ein Array von booleschen Werten konvertiert werden soll.


### <a name="bits--int"></a>Bits: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der Bits in der binären Darstellung von `number` .



## <a name="output--bool"></a>Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)[]

Ein Array von booleschen Werten, die darstellen `number` .

## <a name="remarks"></a>Bemerkungen

Die Eingabe `bits` muss zwischen 0 und 63 liegen.
Die Eingabe `number` muss zwischen 0 und $2 ^ {\texttt{Bits}}-$1 liegen.
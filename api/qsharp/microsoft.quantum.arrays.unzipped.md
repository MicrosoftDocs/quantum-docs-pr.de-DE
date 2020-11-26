---
uid: Microsoft.Quantum.Arrays.Unzipped
title: Entzippte Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Unzipped
qsharp.summary: Given an array of 2-tuples, returns a tuple of two arrays, each containing the elements of the tuples of the input array.
ms.openlocfilehash: aee1d48c9e0a1f104040bc56c78fdbb8bc4d34ba
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219956"
---
# <a name="unzipped-function"></a>Entzippte Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt bei einem Array von 2-Tupeln ein Tupel mit zwei Arrays zurück, die jeweils die Elemente der Tupel des Eingabe Arrays enthalten.

```qsharp
function Unzipped<'T, 'U> (arr : ('T, 'U)[]) : ('T[], 'U[])
```


## <a name="input"></a>Eingabe

### <a name="arr--tu"></a>Arr: ('t, ' U) []

Ein Array, das 2 Tupel enthält.



## <a name="output--tu"></a>Ausgabe: ('t [], ' U [])

Zwei Arrays, das erste-Element, das alle ersten Elemente der eingabetupel enthält, das zweite Array, das alle zweiten Elemente der eingabentupel enthält.

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ des ersten Elements in jedem Tupel.
### <a name="u"></a>"U

Der Typ des zweiten Elements in jedem Tupel.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft.Quantum.Arrays.Zip](xref:Microsoft.Quantum.Arrays.Zipped)
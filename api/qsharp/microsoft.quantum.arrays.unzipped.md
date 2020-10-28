---
uid: Microsoft.Quantum.Arrays.Unzipped
title: Entzippte Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Unzipped
qsharp.summary: Given an array of 2-tuples, returns a tuple of two arrays, each containing the elements of the tuples of the input array.
ms.openlocfilehash: 37c960dc5dbdb8099fbebe1ad63cb44ce642733c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705722"
---
# <a name="unzipped-function"></a>Entzippte Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paketen [](https://nuget.org/packages/)


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
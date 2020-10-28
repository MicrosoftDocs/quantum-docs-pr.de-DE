---
uid: Microsoft.Quantum.Arrays.Zipped
title: ZIP-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zipped
qsharp.summary: Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.
ms.openlocfilehash: 67170fa005675f0e5d788c9c3b350fb9a961a597
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705671"
---
# <a name="zipped-function"></a>ZIP-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paketen [](https://nuget.org/packages/)


Bei zwei Arrays wird ein neues Array von Paaren zurückgegeben, sodass jedes Paar ein Element aus jedem ursprünglichen Array enthält.

```qsharp
function Zipped<'T, 'U> (left : 'T[], right : 'U[]) : ('T, 'U)[]
```


## <a name="input"></a>Eingabe

### <a name="left--t"></a>Left: 't []

Ein Array, das Werte für das erste Element jedes Tupels enthält.


### <a name="right--u"></a>Right: ' U []

Ein Array, das Werte für das zweite Element jedes Tupels enthält.



## <a name="output--tu"></a>Ausgabe: ('t, ' U) []

Ein Array, das Paare des Formulars `(left[idx], right[idx])` für jedes enthält `idx` . Wenn die beiden Arrays nicht die gleiche Länge aufweisen, ist die Ausgabe so lang wie die kürzere der Eingaben.

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ der linken Array Elemente.
### <a name="u"></a>"U

Der Typ der rechten Array Elemente.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft.Quantum.Arrays.ZipPED3](xref:Microsoft.Quantum.Arrays.Zipped3)
- [Microsoft.Quantum.Arrays.Zipped4](xref:Microsoft.Quantum.Arrays.Zipped4)
- [Microsoft. Quantum. Arrays. entzippt](xref:Microsoft.Quantum.Arrays.Unzipped)
---
uid: Microsoft.Quantum.Arrays.MappedByIndex
title: Mappedbyindex-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MappedByIndex
qsharp.summary: Given an array and a function that is defined for the indexed elements of the array, returns a new array that consists of the images of the original array under the function.
ms.openlocfilehash: 07ca523248c363f2229551a14e77803dc4f4f82e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705898"
---
# <a name="mappedbyindex-function"></a>Mappedbyindex-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paketen [](https://nuget.org/packages/)


Gibt ein neues Array zurück, das aus den Bildern des ursprünglichen Arrays unter der Funktion besteht, wenn ein Array und eine Funktion für die indizierten Elemente des Arrays definiert sind.

```qsharp
function MappedByIndex<'T, 'U> (mapper : ((Int, 'T) -> 'U), array : 'T[]) : 'U[]
```


## <a name="input"></a>Eingabe

### <a name="mapper--intt---u"></a>Mapper: ([int](xref:microsoft.quantum.lang-ref.int), t)-> ' U

Eine Funktion von `(Int, 'T)` zu `'U` , die verwendet wird, um Elemente und ihre Indizes zuzuordnen.


### <a name="array--t"></a>Array: 't []

Ein Array von-Elementen `'T` .



## <a name="output--u"></a>Ausgabe: ' U []

Ein Array `'U[]` von-Elementen, die von der-Funktion zugeordnet werden `mapper` .

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ der `array` Elemente.
### <a name="u"></a>"U

Der Ergebnistyp der `mapper` Funktion.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Arrays. zugeordnet](xref:Microsoft.Quantum.Arrays.Mapped)
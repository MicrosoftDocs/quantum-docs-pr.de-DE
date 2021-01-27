---
uid: Microsoft.Quantum.Arrays.MappedByIndex
title: Mappedbyindex-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MappedByIndex
qsharp.summary: Given an array and a function that is defined for the indexed elements of the array, returns a new array that consists of the images of the original array under the function.
ms.openlocfilehash: 584cabcb7b6059ae5d311f13f5f75bd1f87bdba5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845662"
---
# <a name="mappedbyindex-function"></a>Mappedbyindex-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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

## <a name="example"></a>Beispiel

Die folgenden beiden Zeilen sind äquivalent:

```qsharp
let arr = MapIndex(f, [x0, x1, x2]);
```

and

```qsharp
let arr = [f(0, x0), f(1, x1), f(2, x2)];
```

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Arrays. zugeordnet](xref:Microsoft.Quantum.Arrays.Mapped)
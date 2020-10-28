---
uid: Microsoft.Quantum.Arrays.Mapped
title: Zugeordnete Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Mapped
qsharp.summary: Given an array and a function that is defined for the elements of the array, returns a new array that consists of the images of the original array under the function.
ms.openlocfilehash: 1abb9d6fb1a921b49554bef968442f4f2b346b71
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705914"
---
# <a name="mapped-function"></a>Zugeordnete Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paketen [](https://nuget.org/packages/)


Bei Angabe eines Arrays und einer Funktion, die für die Elemente des Arrays definiert ist, wird ein neues Array zurückgegeben, das aus den Bildern des ursprünglichen Arrays unter der Funktion besteht.

```qsharp
function Mapped<'T, 'U> (mapper : ('T -> 'U), array : 'T[]) : 'U[]
```


## <a name="input"></a>Eingabe

### <a name="mapper--t---u"></a>Mapper: 't-> ' U

Eine Funktion von `'T` zu `'U` , die zum Zuordnen von Elementen verwendet wird.


### <a name="array--t"></a>Array: 't []

Ein Array von-Elementen `'T` .



## <a name="output--u"></a>Ausgabe: ' U []

Ein Array `'U[]` von-Elementen, die von der-Funktion zugeordnet werden `mapper` .

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ der `array` Elemente.
### <a name="u"></a>"U

Der Ergebnistyp der `mapper` Funktion.

## <a name="remarks"></a>Hinweise

Die-Funktion ist für generische Typen definiert, d. h., wenn ein Array `'T[]` und eine Funktion vorhanden sind, `mapper: 'T -> 'U` können wir die Elemente des Arrays zuordnen und ein neues Array vom Typ entwickeln `'U[]` .
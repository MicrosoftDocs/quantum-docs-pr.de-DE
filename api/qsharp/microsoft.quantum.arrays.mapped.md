---
uid: Microsoft.Quantum.Arrays.Mapped
title: Zugeordnete Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Mapped
qsharp.summary: Given an array and a function that is defined for the elements of the array, returns a new array that consists of the images of the original array under the function.
ms.openlocfilehash: 00ea0803faf6e8edfa748af63dd6c7e217b1de41
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845689"
---
# <a name="mapped-function"></a>Zugeordnete Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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

## <a name="remarks"></a>Bemerkungen

Die-Funktion ist für generische Typen definiert, d. h., wenn ein Array `'T[]` und eine Funktion vorhanden sind, `mapper: 'T -> 'U` können wir die Elemente des Arrays zuordnen und ein neues Array vom Typ entwickeln `'U[]` .
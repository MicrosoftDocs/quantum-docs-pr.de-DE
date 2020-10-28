---
uid: Microsoft.Quantum.Arrays.MappedOverRange
title: Mappeer doverrange-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MappedOverRange
qsharp.summary: Given a range and a function that takes an integer as input, returns a new array that consists of the images of the range values under the function.
ms.openlocfilehash: e527a3ca1fd7571836f4f79bb453581f53d1db2b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705890"
---
# <a name="mappedoverrange-function"></a>Mappeer doverrange-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paketen [](https://nuget.org/packages/)


Gibt ein neues Array zurück, das aus den Bildern der Bereichs Werte unter der Funktion besteht, wenn ein Bereich und eine Funktion eine ganze Zahl als Eingabe annimmt.

```qsharp
function MappedOverRange<'T> (mapper : (Int -> 'T), range : Range) : 'T[]
```


## <a name="input"></a>Eingabe

### <a name="mapper--int---t"></a>Mapper: [int](xref:microsoft.quantum.lang-ref.int) -> 't

Eine Funktion von `Int` zu `'T` , die zum Zuordnen von Bereichs Werten verwendet wird.


### <a name="range--range"></a>Bereich: [Bereich](xref:microsoft.quantum.lang-ref.range)

Ein Bereich von ganzen Zahlen.



## <a name="output--t"></a>Ausgabe: 't []

Ein Array `'T[]` von-Elementen, die von der-Funktion zugeordnet werden `mapper` .

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Ergebnistyp der `mapper` Funktion.

## <a name="remarks"></a>Hinweise

Die-Funktion ist für generische Typen definiert, d. h., wenn wir über eine Funktion verfügen, `mapper: Int -> 'T` können wir die Werte des Bereichs zuordnen und ein Array vom Typ `'T[]` .

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Arrays. zugeordnet](xref:Microsoft.Quantum.Arrays.Mapped)
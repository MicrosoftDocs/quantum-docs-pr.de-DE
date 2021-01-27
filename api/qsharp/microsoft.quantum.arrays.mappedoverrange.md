---
uid: Microsoft.Quantum.Arrays.MappedOverRange
title: Mappeer doverrange-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MappedOverRange
qsharp.summary: Given a range and a function that takes an integer as input, returns a new array that consists of the images of the range values under the function.
ms.openlocfilehash: 7093043e2a290e6132774b8fe154d3627a254f27
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845652"
---
# <a name="mappedoverrange-function"></a>Mappeer doverrange-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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

## <a name="example"></a>Beispiel

In diesem Beispiel wird 1 zu einem Bereich von geraden Zahlen addiert:

```qsharp
let numbers = MappedOverRange(PlusI(1, _), 0..2..10);
// numbers = [1, 3, 5, 7, 9, 11]
```

## <a name="remarks"></a>Bemerkungen

Die-Funktion ist für generische Typen definiert, d. h., wenn wir über eine Funktion verfügen, `mapper: Int -> 'T` können wir die Werte des Bereichs zuordnen und ein Array vom Typ `'T[]` .

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Arrays. zugeordnet](xref:Microsoft.Quantum.Arrays.Mapped)
---
uid: Microsoft.Quantum.Arrays.Sorted
title: Sortierte Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Sorted
qsharp.summary: Given an array, returns the elements of that array sorted by a given comparison function.
ms.openlocfilehash: bd8b869e03c7f4687c456a944e07a811ae0d2ce2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220228"
---
# <a name="sorted-function"></a>Sortierte Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt bei Angabe eines Arrays die Elemente dieses Arrays nach einer angegebenen Vergleichsfunktion sortiert zurück.

```qsharp
function Sorted<'T> (comparison : (('T, 'T) -> Bool), array : 'T[]) : 'T[]
```


## <a name="input"></a>Eingabe

### <a name="comparison--tt---bool"></a>Vergleich: ('t, 't)-> [bool](xref:microsoft.quantum.lang-ref.bool)

Eine Funktion, die zwei-Elemente als vergleicht, die `a` als kleiner oder gleich angesehen werden, `b` wenn gleich `comparison(a, b)` ist `true` .


### <a name="array--t"></a>Array: 't []

Das Array, das sortiert werden soll.



## <a name="output--t"></a>Ausgabe: 't []



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ der einzelnen Elemente von `array` .

## <a name="remarks"></a>Bemerkungen

Es wird `comparison` davon ausgegangen, dass die Funktion transitiv ist, sodass, wenn `comparison(a, b)` und `comparison(b, c)` , `comparison(a, c)` angenommen wird. Wenn diese Eigenschaft nicht enthalten ist, ist die Ausgabe dieser Funktion möglicherweise falsch.

Da es sich um eine Funktion handelt, sind die Ergebnisse vollständig deternistisch, auch wenn zwei Elemente als gleich betrachtet werden, d `comparison` . h., wenn `comparison(a, b)` und `comparison(b, a)` beide sind `true` .
Insbesondere wird sichergestellt, dass die von dieser Funktion ausgeführte Sortierung stabil ist, sodass, wenn zwei `a` Elemente `b` in dieser Reihenfolge innerhalb von auftreten `array` und als gleich betrachtet werden `comparison` , `a` auch vor `b` in der Ausgabe angezeigt wird.

Beispiel:

```Q#
function LastDigitLessThanOrEqual(left : Int, right : Int) : Bool {
    return LessThanOrEqualI(
        left % 10, right % 10
    );
}

function SortedByLastDigit() : Int[] {
    return Sorted(LastDigitLessThanOrEqual, [3, 37, 11, 17]);
}
// returns [11, 3, 37, 17].
```
---
uid: Microsoft.Quantum.Arrays.Sorted
title: Sortierte Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Sorted
qsharp.summary: Given an array, returns the elements of that array sorted by a given comparison function.
ms.openlocfilehash: cb8a1ef438d798c8201ed9f52677e253770df1d3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845447"
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

## <a name="example"></a>Beispiel

Im folgenden Code Ausschnitt wird ein Array aus ganzen Zahlen sortiert, das in aufsteigender Reihenfolge auftreten soll:

```qsharp
let sortedArray = Sorted(LessThanOrEqualI, [3, 17, 11, -201, -11]);
```

## <a name="remarks"></a>Bemerkungen

Es wird `comparison` davon ausgegangen, dass die Funktion transitiv ist, sodass, wenn `comparison(a, b)` und `comparison(b, c)` , `comparison(a, c)` angenommen wird. Wenn diese Eigenschaft nicht enthalten ist, ist die Ausgabe dieser Funktion möglicherweise falsch.

Da es sich um eine Funktion handelt, sind die Ergebnisse vollständig deternistisch, auch wenn zwei Elemente als gleich betrachtet werden, d `comparison` . h., wenn `comparison(a, b)` und `comparison(b, a)` beide sind `true` .
Insbesondere wird sichergestellt, dass die von dieser Funktion ausgeführte Sortierung stabil ist, sodass, wenn zwei `a` Elemente `b` in dieser Reihenfolge innerhalb von auftreten `array` und als gleich betrachtet werden `comparison` , `a` auch vor `b` in der Ausgabe angezeigt wird.

Beispiel:

```qsharp
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
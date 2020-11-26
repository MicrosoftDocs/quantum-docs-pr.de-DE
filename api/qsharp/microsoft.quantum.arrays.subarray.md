---
uid: Microsoft.Quantum.Arrays.Subarray
title: Subarray-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Subarray
qsharp.summary: Takes an array and a list of locations and produces a new array formed from the elements of the original array that match the given locations.
ms.openlocfilehash: cf72f04421b277ce64354d1eccec11cbc61d78cc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220160"
---
# <a name="subarray-function"></a>Subarray-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Nimmt ein Array und eine Liste von Speicherorten an und erstellt ein neues Array, das aus den Elementen des ursprünglichen Arrays gebildet wird, die den angegebenen Speicherorten entsprechen.

```qsharp
function Subarray<'T> (indices : Int[], array : 'T[]) : 'T[]
```


## <a name="input"></a>Eingabe

### <a name="indices--int"></a>Indizes: [int](xref:microsoft.quantum.lang-ref.int)[]

Eine Liste von ganzen Zahlen, die zum Definieren des Unterarrays verwendet wird.


### <a name="array--t"></a>Array: 't []

Ein Array von-Elementen `'T` .



## <a name="output--t"></a>Ausgabe: 't []

Ein Array `out` von-Elementen, deren Indizes dem Unterarray entsprechen, z `out[idx] == array[indices[idx]]` . b..

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ der `array` Elemente.

## <a name="remarks"></a>Bemerkungen

Die-Funktion ist für generische Typen definiert, d. h., wenn ein Array `'T[]` und eine Liste von Speicherorten vorhanden sind, `Int[]` die das Unterelement definieren.
Die Erstellung des Unterarrays ist eine, die auf der Erstellung einer neuen Deep-Kopie des angegebenen Arrays basiert, anstatt Verweise beizubehalten.

Wenn `Length(indices) < Length(array)` , wird von dieser Funktion eine Teilmenge von zurückgegeben `array` . Wenn dagegen `indices` wiederholte Elemente enthält, werden die entsprechenden Elemente von `array` ebenfalls wiederholt.
Wenn `indices` und `array` dieselbe Länge aufweisen, stellt diese Funktion Permutationen von bereit `array` .
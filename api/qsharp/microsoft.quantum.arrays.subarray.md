---
uid: Microsoft.Quantum.Arrays.Subarray
title: Subarray-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Subarray
qsharp.summary: Takes an array and a list of locations and produces a new array formed from the elements of the original array that match the given locations.
ms.openlocfilehash: be7b6ee1a396d67ebc311d8d97f4bd751a32d171
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705759"
---
# <a name="subarray-function"></a>Subarray-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paketen [](https://nuget.org/packages/)


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

## <a name="remarks"></a>Hinweise

Die-Funktion ist für generische Typen definiert, d. h., wenn ein Array `'T[]` und eine Liste von Speicherorten vorhanden sind, `Int[]` die das Unterelement definieren.
Die Erstellung des Unterarrays ist eine, die auf der Erstellung einer neuen Deep-Kopie des angegebenen Arrays basiert, anstatt Verweise beizubehalten.

Wenn `Length(indices) < Length(array)` , wird von dieser Funktion eine Teilmenge von zurückgegeben `array` . Wenn dagegen `indices` wiederholte Elemente enthält, werden die entsprechenden Elemente von `array` ebenfalls wiederholt.
Wenn `indices` und `array` dieselbe Länge aufweisen, stellt diese Funktion Permutationen von bereit `array` .
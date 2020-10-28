---
uid: Microsoft.Quantum.Arrays.Windows
title: Windows-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Windows
qsharp.summary: Returns all consecutive subarrays of length `size`.
ms.openlocfilehash: 6071d1c3e5981855c57abd0e741b1de0201c30a3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705695"
---
# <a name="windows-function"></a>Windows-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paketen [](https://nuget.org/packages/)


Gibt alle aufeinanderfolgenden Unterarrays der Länge zurück `size` .

```qsharp
function Windows<'T> (size : Int, array : 'T[]) : 'T[][]
```


## <a name="description"></a>BESCHREIBUNG

Diese Funktion gibt alle `n - size + 1` unter Elemente der Länge `size` in der Reihenfolge zurück, wobei `n` die Länge von ist `arr` .
Die ersten unter `arr[0..size - 1], arr[1..size], arr[2..size + 1]` Arrays liegen bis zum letzten Unterarray `arr[n - size..n - 1]` .

Wenn `size <= 0` oder `size > n` , wird ein leeres Array zurückgegeben.

## <a name="input"></a>Eingabe

### <a name="size--int"></a>Größe: [int](xref:microsoft.quantum.lang-ref.int)

Länge der Unterbereiche.


### <a name="array--t"></a>Array: 't []

Ein Array von-Elementen.



## <a name="output--t"></a>Ausgabe: 't [] []



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ der `array` Elemente.
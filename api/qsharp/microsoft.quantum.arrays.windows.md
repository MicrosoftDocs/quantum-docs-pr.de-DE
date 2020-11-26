---
uid: Microsoft.Quantum.Arrays.Windows
title: Windows-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Windows
qsharp.summary: Returns all consecutive subarrays of length `size`.
ms.openlocfilehash: 8f32a23aa4379744b84c3b8d9c8f565e61c3c64e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219888"
---
# <a name="windows-function"></a>Windows-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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
---
uid: Microsoft.Quantum.Arrays.Where
title: Where-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Where
qsharp.summary: Given a predicate and an array, returns the indices of that array where the predicate is true.
ms.openlocfilehash: 1c9fa0463ed49788d12502257d735b965565d1ab
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705698"
---
# <a name="where-function"></a>Where-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paketen [](https://nuget.org/packages/)


Gibt bei Angabe eines Prädikats und eines Arrays die Indizes dieses Arrays zurück, bei denen das Prädikat "true" ist.

```qsharp
function Where<'T> (predicate : ('T -> Bool), array : 'T[]) : Int[]
```


## <a name="input"></a>Eingabe

### <a name="predicate--t---bool"></a>Prädikat: 't-> [bool](xref:microsoft.quantum.lang-ref.bool)

Eine Funktion von `'T` zu einem booleschen Wert, der zum Filtern von Elementen verwendet wird.


### <a name="array--t"></a>Array: 't []

Ein Array von-Elementen `'T` .



## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)[]

Ein Array von Indizes, bei denen " `predicate` true" ist.

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ der `array` Elemente.
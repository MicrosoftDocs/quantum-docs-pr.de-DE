---
uid: Microsoft.Quantum.Arrays.Where
title: Where-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Where
qsharp.summary: Given a predicate and an array, returns the indices of that array where the predicate is true.
ms.openlocfilehash: 97598aa25d2d085aaab94f3d60ee64db9e2b89d6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219922"
---
# <a name="where-function"></a>Where-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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
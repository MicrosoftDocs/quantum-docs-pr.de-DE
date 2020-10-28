---
uid: Microsoft.Quantum.Arrays.EqualA
title: Equala-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: EqualA
qsharp.summary: Given two arrays of the same type and a predicate that is defined for pairs of elements of the arrays, checks whether the arrays are equal.
ms.openlocfilehash: 24fd76aaeb66081d6d8f1eaa3056117f54b5a5e7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706055"
---
# <a name="equala-function"></a>Equala-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paketen [](https://nuget.org/packages/)


Überprüft zwei Arrays desselben Typs und ein Prädikat, das für Paare von Elementen der Arrays definiert ist, und überprüft, ob die Arrays gleich sind.

```qsharp
function EqualA<'T> (equal : (('T, 'T) -> Bool), array1 : 'T[], array2 : 'T[]) : Bool
```


## <a name="input"></a>Eingabe

### <a name="equal--tt---bool"></a>gleich: ('t, 't)-> [bool](xref:microsoft.quantum.lang-ref.bool)

Eine Funktion von Tupel `('T, 'T)` auf `Bool` , die verwendet wird, um zu überprüfen, ob zwei Elemente von Arrays gleich sind.


### <a name="array1--t"></a>array1: 't []

Das erste Array, das verglichen werden soll.


### <a name="array2--t"></a>array2: 't []

Das zweite Array, das verglichen werden soll.



## <a name="output--bool"></a>Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)

Der `true` -Wert nur dann, wenn `array1` und `array2` gleich sind.
Das heißt, wenn beide Arrays die gleiche Länge aufweisen und alle Elemente gleich sind, wie von definiert `equal` .

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ der Elemente des Arrays.

## <a name="remarks"></a>Hinweise

Diese Funktion ist für generische Typen definiert. Wenn also zwei Arrays `'T[]` und eine Funktion vorhanden sind `equal: ('T, 'T) -> Bool` , gibt diese Funktion einen Wert zurück, `Bool` der angibt, ob die Arrays gleich sind.
Damit zwei Arrays als gleich betrachtet werden, müssen Sie die gleiche Länge aufweisen, und die Elemente an denselben Positionen in den Arrays müssen gleich sein.
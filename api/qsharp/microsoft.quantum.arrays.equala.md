---
uid: Microsoft.Quantum.Arrays.EqualA
title: Equala-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: EqualA
qsharp.summary: Given two arrays of the same type and a predicate that is defined for pairs of elements of the arrays, checks whether the arrays are equal.
ms.openlocfilehash: fe22e208f67d2c289b0b2d99f19ff26fc5abc3d8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848688"
---
# <a name="equala-function"></a>Equala-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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

## <a name="example"></a>Beispiel

Der folgende Code überprüft, ob verschiedene Paare von Arrays gleich sind:

```qsharp
open Microsoft.Quantum.Arrays;
open Microsoft.Quantum.Logical;

function EqualADemo() : Unit {
    let equalArrays = EqualA(EqualI, [2, 3, 4], [2, 3, 4]);
    let differentLength = EqualA(EqualD, [2.0, 3.0, 4.0], [2.0, 3.0]);
    let differentElements = EqualA(EqualR, [One, Zero], [One, One]);
    Message($"Equal arrays are {equalArrays ? "equal" | "not equal"}");
    Message($"Arrays of different length are {differentLength ? "equal" | "not equal"}");
    Message($"Arrays of the same length with different elements are {differentElements ? "equal" | "not equal"}");
}
```

## <a name="remarks"></a>Bemerkungen

Diese Funktion ist für generische Typen definiert. Wenn also zwei Arrays `'T[]` und eine Funktion vorhanden sind `equal: ('T, 'T) -> Bool` , gibt diese Funktion einen Wert zurück, `Bool` der angibt, ob die Arrays gleich sind.
Damit zwei Arrays als gleich betrachtet werden, müssen Sie die gleiche Länge aufweisen, und die Elemente an denselben Positionen in den Arrays müssen gleich sein.
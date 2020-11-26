---
uid: Microsoft.Quantum.Arrays.Zipped3
title: Zipped3-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zipped3
qsharp.summary: Given three arrays, returns a new array of 3-tuples such that each 3-tuple contains an element from each original array.
ms.openlocfilehash: 37fda4082a46870270414649f807659fa561962b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219684"
---
# <a name="zipped3-function"></a>Zipped3-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Bei drei Arrays gibt ein neues Array von 3-Tupeln zurück, sodass jedes 3-Tupel ein Element aus jedem ursprünglichen Array enthält.

```qsharp
function Zipped3<'T1, 'T2, 'T3> (first : 'T1[], second : 'T2[], third : 'T3[]) : ('T1, 'T2, 'T3)[]
```


## <a name="input"></a>Eingabe

### <a name="first--t1"></a>zuerst: 't 1 []

Ein Array, das Werte für das erste Element jedes Tupels enthält.


### <a name="second--t2"></a>Zweitens: 't 2 []

Ein Array, das Werte für das zweite Element jedes Tupels enthält.


### <a name="third--t3"></a>Drittens: 't 3 []

Ein Array, das Werte für das dritte Element jedes Tupels enthält.



## <a name="output--t1t2t3"></a>Ausgabe: ('t 1, 't 2, 't 3) []

Ein Array, das jeweils 3 Tupel des Formulars enthält `(first[idx], second[idx], third[idx])` `idx` . Wenn die drei Arrays nicht die gleiche Länge aufweisen, ist die Ausgabe so lang wie die kürzere der Eingaben.

## <a name="type-parameters"></a>Typparameter

### <a name="t1"></a>Nicht 1

Der Typ der ersten Array Elemente.
### <a name="t2"></a>Nicht 2

Der Typ der zweiten Array Elemente.
### <a name="t3"></a>Nicht 3

Der Typ der dritten Array Elemente.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft.Quantum.Arrays.Zip](xref:Microsoft.Quantum.Arrays.Zipped)
- [Microsoft.Quantum.Arrays.Zipped4](xref:Microsoft.Quantum.Arrays.Zipped4)
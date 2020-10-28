---
uid: Microsoft.Quantum.Arrays.Zip4
title: Zip4-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zip4
qsharp.summary: >-
  > [!WARNING]

  > Zip4 has been deprecated. Please use <xref:Microsoft.Quantum.Arrays.Zipped4> instead.


  Given four arrays, returns a new array of 4-tuples such that each 4-tuple contains an element from each original array.
ms.openlocfilehash: d42b3b6db059163f6c766d4f133551be293c153d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705663"
---
# <a name="zip4-function"></a>Zip4-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paketen [](https://nuget.org/packages/)


> [!WARNING]
> Zip4 wurde als veraltet markiert. Verwenden Sie stattdessen <xref:Microsoft.Quantum.Arrays.Zipped4>.

Bei Angabe von vier Arrays wird ein neues Array von 4-Tupeln zurückgegeben, sodass jedes 4-Tupel ein Element aus jedem ursprünglichen Array enthält.

```qsharp
function Zip4<'T1, 'T2, 'T3, 'T4> (first : 'T1[], second : 'T2[], third : 'T3[], fourth : 'T4[]) : ('T1, 'T2, 'T3, 'T4)[]
```


## <a name="input"></a>Eingabe

### <a name="first--t1"></a>zuerst: 't 1 []

Ein Array, das Werte für das erste Element jedes Tupels enthält.


### <a name="second--t2"></a>Zweitens: 't 2 []

Ein Array, das Werte für das zweite Element jedes Tupels enthält.


### <a name="third--t3"></a>Drittens: 't 3 []

Ein Array, das Werte für das dritte Element jedes Tupels enthält.


### <a name="fourth--t4"></a>Fourth: 't 4 []

Ein Array, das Werte für das vierte Element jedes Tupels enthält.



## <a name="output--t1t2t3t4"></a>Ausgabe: ('t 1, 't 2, 't 3, 't 4) []

Ein Array, das 4 Tupel des Formulars `(first[idx], second[idx], third[idx], fourth[idx])` für jedes enthält `idx` . Wenn die vier Arrays nicht die gleiche Länge aufweisen, ist die Ausgabe so lang wie die kürzere der Eingaben.

## <a name="type-parameters"></a>Typparameter

### <a name="t1"></a>Nicht 1

Der Typ der ersten Array Elemente.
### <a name="t2"></a>Nicht 2

Der Typ der zweiten Array Elemente.
### <a name="t3"></a>Nicht 3

Der Typ der dritten Array Elemente.
### <a name="t4"></a>'T 4

Der Typ der vierten Array Elemente.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft.Quantum.Arrays.Zip](xref:Microsoft.Quantum.Arrays.Zip)
- [Microsoft.Quantum.Arrays.Zip3](xref:Microsoft.Quantum.Arrays.Zip3)
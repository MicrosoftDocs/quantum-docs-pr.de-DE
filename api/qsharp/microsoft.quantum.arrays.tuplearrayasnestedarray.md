---
uid: Microsoft.Quantum.Arrays.TupleArrayAsNestedArray
title: Tuplearrayasnetstedarray-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: TupleArrayAsNestedArray
qsharp.summary: Turns a list of 2-tuples into a nested array.
ms.openlocfilehash: c898178b6385b27f753509f0748a8b666b5066bd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220075"
---
# <a name="tuplearrayasnestedarray-function"></a>Tuplearrayasnetstedarray-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Wandelt eine Liste von 2 Tupeln in ein Array um.

```qsharp
function TupleArrayAsNestedArray<'T> (tupleList : ('T, 'T)[]) : 'T[][]
```


## <a name="input"></a>Eingabe

### <a name="tuplelist--tt"></a>tuplelist: ('t, 't) []

Liste von 2-Tupeln, die in ein Array umgewandelt werden sollen.



## <a name="output--t"></a>Ausgabe: 't [] []

Ein geschachtelte Array mit einer Länge, die der tuplelist entspricht.

## <a name="example"></a>Beispiel

```qsharp
// The following returns [[2, 3], [4, 5]]
TupleArrayAsNestedArray([(2, 3), (4, 5)]);
```

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF


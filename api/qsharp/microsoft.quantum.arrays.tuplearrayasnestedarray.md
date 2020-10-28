---
uid: Microsoft.Quantum.Arrays.TupleArrayAsNestedArray
title: Tuplearrayasnetstedarray-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: TupleArrayAsNestedArray
qsharp.summary: Turns a list of 2-tuples into a nested array.
ms.openlocfilehash: 917f35db949790ab3ae6e7a2184bcfcf5ed50be6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705735"
---
# <a name="tuplearrayasnestedarray-function"></a>Tuplearrayasnetstedarray-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paketen [](https://nuget.org/packages/)


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


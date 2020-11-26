---
uid: Microsoft.Quantum.Arrays.Partitioned
title: Partitionierte Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Partitioned
qsharp.summary: Splits an array into multiple parts.
ms.openlocfilehash: bce46262e3ef64a43e578098d81c5dd39225915e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220500"
---
# <a name="partitioned-function"></a>Partitionierte Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Teilt ein Array in mehrere Teile auf.

```qsharp
function Partitioned<'T> (nElements : Int[], arr : 'T[]) : 'T[][]
```


## <a name="input"></a>Eingabe

### <a name="nelements--int"></a>nelements: [int](xref:microsoft.quantum.lang-ref.int)[]

Anzahl von Elementen in jedem Teil des Arrays


### <a name="arr--t"></a>Arr: 't []

Eingabe Array, das aufgeteilt werden soll.



## <a name="output--t"></a>Ausgabe: 't [] []

Mehrere Arrays, bei denen das erste Array der `nElements[0]` erste `arr` und das zweite Array das nächste `nElements[1]` von `arr` usw. ist. Das letzte Array enthält alle verbleibenden Elemente.

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF


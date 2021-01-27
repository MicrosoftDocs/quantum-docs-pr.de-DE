---
uid: Microsoft.Quantum.Arrays.Partitioned
title: Partitionierte Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Partitioned
qsharp.summary: Splits an array into multiple parts.
ms.openlocfilehash: 43d99a0e33a813e4af23a3890ace808e91c1049c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845537"
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



## <a name="example"></a>Beispiel

```qsharp
// The following returns [[1, 5], [3], [7]];
let split = Partitioned([2,1], [1,5,3,7]);
```
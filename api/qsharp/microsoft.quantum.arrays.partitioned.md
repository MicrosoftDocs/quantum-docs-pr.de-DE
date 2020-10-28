---
uid: Microsoft.Quantum.Arrays.Partitioned
title: Partitionierte Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Partitioned
qsharp.summary: Splits an array into multiple parts.
ms.openlocfilehash: e3395afeda206e255a58175b57245f91c588d978
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705847"
---
# <a name="partitioned-function"></a>Partitionierte Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paketen [](https://nuget.org/packages/)


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


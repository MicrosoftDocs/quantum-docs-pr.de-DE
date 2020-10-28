---
uid: Microsoft.Quantum.Arrays.HeadAndRest
title: Headandrest-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: HeadAndRest
qsharp.summary: Returns a tuple of first and all remaining elements of the array.
ms.openlocfilehash: 9af4ba48a21d3cdf932b2f702051a70a6108db1b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705983"
---
# <a name="headandrest-function"></a>Headandrest-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paketen [](https://nuget.org/packages/)


Gibt ein Tupel mit dem ersten und allen verbleibenden Elementen des Arrays zurück.

```qsharp
function HeadAndRest<'A> (array : 'A[]) : ('A, 'A[])
```


## <a name="input"></a>Eingabe

### <a name="array--a"></a>Array: ' A []

Ein Array mit mindestens einem Element.



## <a name="output--aa"></a>Ausgabe: ("a", "a" [])

Ein Tupel mit dem ersten und allen verbleibenden Elementen des Arrays.

## <a name="type-parameters"></a>Typparameter

### <a name="a"></a>"A

Der Typ der Arrayelemente.
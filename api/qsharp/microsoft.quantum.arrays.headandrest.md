---
uid: Microsoft.Quantum.Arrays.HeadAndRest
title: Headandrest-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: HeadAndRest
qsharp.summary: Returns a tuple of first and all remaining elements of the array.
ms.openlocfilehash: 1144e00227df1cd7d96bc76b118b0b556adbaa96
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221078"
---
# <a name="headandrest-function"></a>Headandrest-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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
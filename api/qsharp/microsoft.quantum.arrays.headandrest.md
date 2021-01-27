---
uid: Microsoft.Quantum.Arrays.HeadAndRest
title: Headandrest-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: HeadAndRest
qsharp.summary: Returns a tuple of first and all remaining elements of the array.
ms.openlocfilehash: c082e0a917343c18e5f511f065b2e78f1e217ecc
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848561"
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
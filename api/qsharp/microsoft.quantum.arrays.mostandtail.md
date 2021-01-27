---
uid: Microsoft.Quantum.Arrays.MostAndTail
title: "\"Mustandtail\"-Funktion"
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MostAndTail
qsharp.summary: Returns a tuple of all but one and the last element of the array.
ms.openlocfilehash: fd5569f1b71ac2fdf2b5c08ba7dde172e3a6744e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845600"
---
# <a name="mostandtail-function"></a>"Mustandtail"-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt ein Tupel von allen bis auf ein und das letzte Element des Arrays zurück.

```qsharp
function MostAndTail<'A> (array : 'A[]) : ('A[], 'A)
```


## <a name="input"></a>Eingabe

### <a name="array--a"></a>Array: ' A []

Ein Array mit mindestens einem Element.



## <a name="output--aa"></a>Ausgabe: (' a [], ' a ')

Ein Tupel von allen bis auf ein und das letzte Element des Arrays.

## <a name="type-parameters"></a>Typparameter

### <a name="a"></a>"A

Der Typ der Arrayelemente.
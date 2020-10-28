---
uid: Microsoft.Quantum.Arrays.MostAndTail
title: "\"Mustandtail\"-Funktion"
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MostAndTail
qsharp.summary: Returns a tuple of all but one and the last element of the array.
ms.openlocfilehash: 8786250cf2f78ce2e9ff8baddc856d0bc07cb9a0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705858"
---
# <a name="mostandtail-function"></a>"Mustandtail"-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paketen [](https://nuget.org/packages/)


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
---
uid: Microsoft.Quantum.Arrays.Enumerated
title: Enumerierte Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Enumerated
qsharp.summary: Given an array, returns a new array containing elements of the original array along with the indices of each element.
ms.openlocfilehash: 0a591025a4eef79e08b47527c0bdb556f5645334
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706066"
---
# <a name="enumerated-function"></a>Enumerierte Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paketen [](https://nuget.org/packages/)


Gibt bei Angabe eines Arrays ein neues Array zurück, das die Elemente des ursprünglichen Arrays zusammen mit den Indizes der einzelnen Elemente enthält.

```qsharp
function Enumerated<'TElement> (array : 'TElement[]) : (Int, 'TElement)[]
```


## <a name="input"></a>Eingabe

### <a name="array--telement"></a>Array: ' telements []

Ein Array, dessen Elemente aufgelistet werden sollen.



## <a name="output--inttelement"></a>Ausgabe: ([int](xref:microsoft.quantum.lang-ref.int), ' telements) []

Ein neues Array, das Elemente des ursprünglichen Arrays zusammen mit ihren Indizes enthält.

## <a name="type-parameters"></a>Typparameter

### <a name="telement"></a>' Telements '

Der Typ der Elemente des Arrays.
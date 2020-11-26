---
uid: Microsoft.Quantum.Arrays.Enumerated
title: Enumerierte Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Enumerated
qsharp.summary: Given an array, returns a new array containing elements of the original array along with the indices of each element.
ms.openlocfilehash: 94e8fdb7288bc43ed84d10a3292819b455a2be31
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221418"
---
# <a name="enumerated-function"></a>Enumerierte Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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
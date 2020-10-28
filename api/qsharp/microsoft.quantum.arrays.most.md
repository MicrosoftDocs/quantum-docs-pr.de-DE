---
uid: Microsoft.Quantum.Arrays.Most
title: Most-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Most
qsharp.summary: Creates an array that is equal to an input array except that the last array element is dropped.
ms.openlocfilehash: ca89041a4e70472e9bf7a63ffcacccb35aad527c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705863"
---
# <a name="most-function"></a>Most-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paketen [](https://nuget.org/packages/)


Erstellt ein Array, das gleich einem Eingabe Array ist, mit dem Unterschied, dass das letzte Array Element gelöscht wird.

```qsharp
function Most<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a>Eingabe

### <a name="array--t"></a>Array: 't []

Ein Array, dessen erstes bis zu letztes Element das Ausgabe Array bilden soll.



## <a name="output--t"></a>Ausgabe: 't []

Ein Array, das die Elemente enthält `array[0..Length(array) - 2]` .

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ der Arrayelemente.
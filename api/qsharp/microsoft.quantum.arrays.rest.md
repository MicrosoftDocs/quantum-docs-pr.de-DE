---
uid: Microsoft.Quantum.Arrays.Rest
title: Rest-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Rest
qsharp.summary: Creates an array that is equal to an input array except that the first array element is dropped.
ms.openlocfilehash: 4dd10b6e8839fd906ca9c2e36c89c626d5772149
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220389"
---
# <a name="rest-function"></a>Rest-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Erstellt ein Array, das gleich einem Eingabe Array ist, außer dass das erste Array Element gelöscht wird.

```qsharp
function Rest<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a>Eingabe

### <a name="array--t"></a>Array: 't []

Ein Array, dessen zweites bis letztes Element das Ausgabe Array bilden soll.



## <a name="output--t"></a>Ausgabe: 't []

Ein Array, das die Elemente enthält `array[1..Length(array) - 1]` .

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ der Arrayelemente.
---
uid: Microsoft.Quantum.Arrays.Rest
title: Rest-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Rest
qsharp.summary: Creates an array that is equal to an input array except that the first array element is dropped.
ms.openlocfilehash: c14e4b2902741d7ea70c895aa715cbcaa849af3e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705807"
---
# <a name="rest-function"></a>Rest-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paketen [](https://nuget.org/packages/)


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
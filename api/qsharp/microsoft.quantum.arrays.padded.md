---
uid: Microsoft.Quantum.Arrays.Padded
title: Aufgefüllte Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Padded
qsharp.summary: Returns an array padded at with specified values up to a specified length.
ms.openlocfilehash: 2b7a80d1cf5c82a1ff52bc4aa207cfe335b40061
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220534"
---
# <a name="padded-function"></a>Aufgefüllte Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt ein Array zurück, das bei mit angegebenen Werten bis zu einer angegebenen Länge aufgefüllt wird.

```qsharp
function Padded<'T> (nElementsTotal : Int, defaultElement : 'T, inputArray : 'T[]) : 'T[]
```


## <a name="input"></a>Eingabe

### <a name="nelementstotal--int"></a>nelementstotal: [int](xref:microsoft.quantum.lang-ref.int)

Die Länge des aufgefüllten Arrays. Wenn dies positiv ist, `inputArray` wird am Kopf aufgefüllt. Wenn diese negative Zahl ist, `inputArray` wird am Ende aufgefüllt.


### <a name="defaultelement--t"></a>defaultelements: 't

Der Standardwert, der für Auffüll Elemente verwendet werden soll.


### <a name="inputarray--t"></a>Input Array: 't []

Array, dessen Werte sich an der Spitze des Ausgabe Arrays befinden.



## <a name="output--t"></a>Ausgabe: 't []

Ein Array `output` , das `inputArray` an der Kopfzeile mit `defaultElement` s bis zu der Länge aufgefüllt wird `output` . `nElementsTotal`

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ der Arrayelemente.
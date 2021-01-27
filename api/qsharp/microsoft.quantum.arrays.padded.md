---
uid: Microsoft.Quantum.Arrays.Padded
title: Aufgefüllte Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Padded
qsharp.summary: Returns an array padded at with specified values up to a specified length.
ms.openlocfilehash: 556e5f5175ee54470a99f32c037eeb2cd80588d0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845560"
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

## <a name="example"></a>Beispiel

```qsharp
let array = [10, 11, 12];
// The following line returns [10, 12, 15, 2, 2, 2].
let output = Padded(-6, array, 2);
// The following line returns [2, 2, 2, 10, 12, 15].
let output = Padded(6, array, 2);
```
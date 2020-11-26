---
uid: Microsoft.Quantum.Arrays.FlatMapped
title: Flatmapping-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: FlatMapped
qsharp.summary: Given an array and a function that maps an array element to some output array, returns the concatenated output arrays for each array element.
ms.openlocfilehash: e851e8503b3afcb4572f09fe39079247518c22c4
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221248"
---
# <a name="flatmapped-function"></a>Flatmapping-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt bei einem Array und einer Funktion, die ein Array Element einem Ausgabe Array zuordnet, die verketteten Ausgabe Arrays für jedes Array Element zurück.

```qsharp
function FlatMapped<'TInput, 'TOutput> (mapper : ('TInput -> 'TOutput[]), array : 'TInput[]) : 'TOutput[]
```


## <a name="input"></a>Eingabe

### <a name="mapper--tinput---toutput"></a>Mapper: ' TInput-> ' TOutput []

Eine Funktion von `'TInput` zu `'TOutput[]` , die zum Zuordnen von Array Elementen verwendet wird.


### <a name="array--tinput"></a>Array: ' TInput []

Ein Array von-Elementen.



## <a name="output--toutput"></a>Ausgabe: ' TOutput []

Ein Array von `'TOutput[]` , bei dem es sich um die Verkettung aller von der Zuordnungs Funktion generierten Arrays handelt.

## <a name="type-parameters"></a>Typparameter

### <a name="tinput"></a>' TInput

Der Typ der `array` Elemente.
### <a name="toutput"></a>"TOutput"

Die- `mapper` Funktion gibt Arrays dieses Typs zurück.
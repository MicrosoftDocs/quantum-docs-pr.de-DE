---
uid: Microsoft.Quantum.Arrays.FlatMapped
title: Flatmapping-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: FlatMapped
qsharp.summary: Given an array and a function that maps an array element to some output array, returns the concatenated output arrays for each array element.
ms.openlocfilehash: bee7002c5a1e80cee7907ff9cb4ebaaedf8e9923
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848638"
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

## <a name="example"></a>Beispiel

```qsharp
let Numbers = SequenceI(1, _); // generates numbers starting from 1
let values = FlatMapped(Numbers, [1, 2, 3]);
// values = [1, 1, 2, 1, 2, 3]
```
---
uid: Microsoft.Quantum.Arrays.ForEach
title: Foreach-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ForEach
qsharp.summary: Given an array and an operation that is defined for the elements of the array, returns a new array that consists of the images of the original array under the operation.
ms.openlocfilehash: ab6ac6eb913095f31ba166ac27f034f2e2875acf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705999"
---
# <a name="foreach-operation"></a>Foreach-Vorgang

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paketen [](https://nuget.org/packages/)


Gibt ein neues Array zurück, das aus den Bildern des ursprünglichen Arrays unter dem Vorgang besteht, wenn ein Array und ein Vorgang angegeben sind, der für die Elemente des Arrays definiert ist.

```qsharp
operation ForEach<'T, 'U> (action : ('T => 'U), array : 'T[]) : 'U[]
```


## <a name="input"></a>Eingabe

### <a name="action--t--u"></a>Aktion: 't => ' U 

Ein Vorgang von `'T` bis `'U` , der auf jedes Element angewendet wird.


### <a name="array--t"></a>Array: 't []

Ein Array von-Elementen `'T` .



## <a name="output--u"></a>Ausgabe: ' U []

Ein Array `'U[]` von-Elementen, die durch den-Vorgang zugeordnet werden `action` .

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ der `array` Elemente.
### <a name="u"></a>"U

Der Ergebnistyp des `action` Vorgangs.

## <a name="remarks"></a>Hinweise

Der Vorgang ist für generische Typen definiert, d. h., wenn wir ein Array `'T[]` und einen Vorgang haben, `action : 'T -> 'U` können wir die Elemente des Arrays zuordnen und ein neues Array vom Typ entwickeln `'U[]` .
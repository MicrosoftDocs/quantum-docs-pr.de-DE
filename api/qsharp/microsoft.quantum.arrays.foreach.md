---
uid: Microsoft.Quantum.Arrays.ForEach
title: Foreach-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ForEach
qsharp.summary: Given an array and an operation that is defined for the elements of the array, returns a new array that consists of the images of the original array under the operation.
ms.openlocfilehash: 90dd6f94408d37d2b32d82e772a482b0e69c523f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848582"
---
# <a name="foreach-operation"></a>Foreach-Vorgang

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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

## <a name="remarks"></a>Bemerkungen

Der Vorgang ist für generische Typen definiert, d. h., wenn wir ein Array `'T[]` und einen Vorgang haben, `action : 'T -> 'U` können wir die Elemente des Arrays zuordnen und ein neues Array vom Typ entwickeln `'U[]` .
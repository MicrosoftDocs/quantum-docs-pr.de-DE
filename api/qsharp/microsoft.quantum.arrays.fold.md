---
uid: Microsoft.Quantum.Arrays.Fold
title: Fold-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Fold
qsharp.summary: Iterates a function `f` through an array `array`, returning `f(f(f(initialState, array[0]), array[1]), ...)`.
ms.openlocfilehash: a42f9a832c18bd612c1ae416187f3f2513eed54d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221163"
---
# <a name="fold-function"></a>Fold-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Iteriert eine Funktion `f` durch ein Array `array` und gibt zurück `f(f(f(initialState, array[0]), array[1]), ...)` .

```qsharp
function Fold<'State, 'T> (folder : (('State, 'T) -> 'State), state : 'State, array : 'T[]) : 'State
```


## <a name="input"></a>Eingabe

### <a name="folder--statet---state"></a>Ordner: (' State, 't)-> ' State

Eine Funktion, die über das Array gefaltet werden soll.


### <a name="state--state"></a>Status: "State"

Der anfängliche Zustand des Ordners.


### <a name="array--t"></a>Array: 't []

Ein Array von Werten, die zusammengeführt werden sollen.



## <a name="output--state"></a>Ausgabe: "State

Der endgültige Zustand, der vom Ordner nach dem Durchlaufen aller Elemente von zurückgegeben wird `array` .

## <a name="type-parameters"></a>Typparameter

### <a name="state"></a>"State"

Der Typ der Zustände `folder` , mit denen die Funktion arbeitet, d. h., akzeptiert als erstes Argument und gibt zurück.
### <a name="t"></a>GIF

Der Typ der `array` Elemente.
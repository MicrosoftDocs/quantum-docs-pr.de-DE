---
uid: Microsoft.Quantum.Arrays.Fold
title: Fold-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Fold
qsharp.summary: Iterates a function `f` through an array `array`, returning `f(f(f(initialState, array[0]), array[1]), ...)`.
ms.openlocfilehash: 47c23dd657391d80fe473d98f2036d8ddf1dbb0b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706002"
---
# <a name="fold-function"></a>Fold-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paketen [](https://nuget.org/packages/)


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
---
uid: Microsoft.Quantum.Arrays.Fold
title: Fold-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Fold
qsharp.summary: Iterates a function `f` through an array `array`, returning `f(f(f(initialState, array[0]), array[1]), ...)`.
ms.openlocfilehash: d12e070058178ce2cbdd70cade5bc16607a55d5e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848601"
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

## <a name="example"></a>Beispiel

```qsharp
function Plus(a : Double, b : Double) {
    return a + b;
}
function Sum(xs : Double[]) {
    return Fold(Plus, 0.0, xs);
}
```
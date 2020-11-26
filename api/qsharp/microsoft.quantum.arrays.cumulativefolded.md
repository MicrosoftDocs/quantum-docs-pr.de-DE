---
uid: Microsoft.Quantum.Arrays.CumulativeFolded
title: Kumuativegefaltete Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: CumulativeFolded
qsharp.summary: Combines Mapped and Fold into a single function
ms.openlocfilehash: ffb934d06f6be06cbc35a523c90d2c54e0a51353
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210028"
---
# <a name="cumulativefolded-function"></a>Kumuativegefaltete Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Kombiniert zugeordnete und Fold in einer einzelnen Funktion

```qsharp
function CumulativeFolded<'State, 'T> (fn : (('State, 'T) -> 'State), state : 'State, array : 'T[]) : 'State[]
```


## <a name="description"></a>BESCHREIBUNG

Diese Funktion durchläuft die `fn` Funktion durch das Array, beginnend bei einem Anfangszustand `state` und gibt alle Zwischenwerte zurück, ohne den Anfangszustand.

## <a name="input"></a>Eingabe

### <a name="fn--statet---state"></a>FN: (' State, 't)-> ' State

Eine Funktion, die über das Array gefaltet werden soll.


### <a name="state--state"></a>Status: "State"

Der anfängliche Zustand, der gefaltet werden soll.


### <a name="array--t"></a>Array: 't []

Ein Array von Werten, die zusammengeführt werden sollen.



## <a name="output--state"></a>Ausgabe: ' State []

Alle Zwischenzustände, einschließlich des Endzustands, jedoch nicht der Anfangszustand.
Die Länge des Ausgabe Arrays hat dieselbe Länge wie `array` .

## <a name="type-parameters"></a>Typparameter

### <a name="state"></a>"State"

Der Typ der Zustände, mit denen die `fn` Funktion arbeitet, d. h., akzeptiert als erste Eingabe und gibt zurück.
### <a name="t"></a>GIF

Der Typ der `array` Elemente.
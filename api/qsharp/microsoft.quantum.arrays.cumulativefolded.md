---
uid: Microsoft.Quantum.Arrays.CumulativeFolded
title: Kumuativegefaltete Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: CumulativeFolded
qsharp.summary: Combines Mapped and Fold into a single function
ms.openlocfilehash: a09c2779c8f06d8f6b7b0902366f3cefbbca4525
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706127"
---
# <a name="cumulativefolded-function"></a>Kumuativegefaltete Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paketen [](https://nuget.org/packages/)


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
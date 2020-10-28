---
uid: Microsoft.Quantum.Logical.LexographicComparison
title: Lexographiccomparison-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LexographicComparison
qsharp.summary: Given a comparison function, returns a new function that lexographically compares two arrays.
ms.openlocfilehash: f0b68974a0ea26907b58971e4fa4b1f06f5714d2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701441"
---
# <a name="lexographiccomparison-function"></a>Lexographiccomparison-Funktion

Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Paketen [](https://nuget.org/packages/)


Gibt eine-Vergleichsfunktion zurück, die eine neue Funktion zurückgibt, die zwei Arrays lexografisch vergleicht.

```qsharp
function LexographicComparison<'T> (elementComparison : (('T, 'T) -> Bool)) : (('T[], 'T[]) -> Bool)
```


## <a name="input"></a>Eingabe

### <a name="elementcomparison--tt---bool"></a>Element Comparison: ('t, 't)-> [bool](xref:microsoft.quantum.lang-ref.bool)

Eine Funktion, die zwei Elemente `x` und vergleicht und `y` zurückgibt, wenn `x` kleiner oder gleich ist `y` .



## <a name="output--tt---bool"></a>Ausgabe: ('t [], 't [])-> [bool](xref:microsoft.quantum.lang-ref.bool)

Eine Funktion, die zwei Arrays `xs` und vergleicht und `ys` zurückgibt, wenn `xs` vor oder gleich `ys` in der lexographical-Reihenfolge auftritt.

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ der Elemente der zu vergleichenden Arrays.

## <a name="remarks"></a>Hinweise

Der lexografischen Vergleich zwischen zwei Arrays `xs` und `ys` wird durch die folgende Prozedur definiert. Wir sagen, dass zwei Elemente `x` und `y` äquivalent sind, wenn `elementComparison(x, y)` und beide "true" `elementComparison(y, x)` sind.

- Beide Arrays werden Element-für-Element-Elemente verglichen, bis das erste Paar Elemente, die nicht äquivalent sind. Das Array, das das Element enthält, das zuerst anhand von auftritt, `elementComparison` wird als erstes in der lexographical-Reihenfolge angezeigt.
- Wenn keine nicht gleichwertigen Elemente gefunden werden und ein Array länger als das andere ist, wird das kürzere Array als erstes Vorkommen bezeichnet.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Arrays. sortiert](xref:Microsoft.Quantum.Arrays.Sorted)
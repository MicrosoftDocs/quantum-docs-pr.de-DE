---
uid: Microsoft.Quantum.Logical.LexographicComparison
title: Lexographiccomparison-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LexographicComparison
qsharp.summary: Given a comparison function, returns a new function that lexographically compares two arrays.
ms.openlocfilehash: de8179ab6e835d08e7f41287f31a876b7ecc91c5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98814379"
---
# <a name="lexographiccomparison-function"></a>Lexographiccomparison-Funktion

Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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

## <a name="remarks"></a>Bemerkungen

Der lexografischen Vergleich zwischen zwei Arrays `xs` und `ys` wird durch die folgende Prozedur definiert. Wir sagen, dass zwei Elemente `x` und `y` äquivalent sind, wenn `elementComparison(x, y)` und beide "true" `elementComparison(y, x)` sind.

- Beide Arrays werden Element-für-Element-Elemente verglichen, bis das erste Paar Elemente, die nicht äquivalent sind. Das Array, das das Element enthält, das zuerst anhand von auftritt, `elementComparison` wird als erstes in der lexographical-Reihenfolge angezeigt.
- Wenn keine nicht gleichwertigen Elemente gefunden werden und ein Array länger als das andere ist, wird das kürzere Array als erstes Vorkommen bezeichnet.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Arrays. sortiert](xref:Microsoft.Quantum.Arrays.Sorted)
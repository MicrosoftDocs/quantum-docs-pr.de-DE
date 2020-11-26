---
uid: Microsoft.Quantum.Arrays.RectangularArrayFact
title: Rechgulararrayfact-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: RectangularArrayFact
qsharp.summary: Represents a condition that a 2-dimensional array has a rectangular shape
ms.openlocfilehash: b8ef7d52f7f815ca3e21ded1236e775a381646cb
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220415"
---
# <a name="rectangulararrayfact-function"></a>Rechgulararrayfact-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Stellt eine Bedingung dar, dass ein zweidimensionales Array eine rechteckige Form aufweist.

```qsharp
function RectangularArrayFact<'T> (array : 'T[][], message : String) : Unit
```


## <a name="description"></a>BESCHREIBUNG

Diese Funktion bestätigt, dass jede Zeile in einem Array die gleiche Länge aufweist.

## <a name="input"></a>Eingabe

### <a name="array--t"></a>Array: 't [] []

Ein zweidimensionales Array von-Elementen.


### <a name="message--string"></a>Message: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)

Eine Meldung, die gedruckt werden soll, wenn das Array kein rechteckiges Array ist



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ der einzelnen Elemente von `array` .

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Arrays. squarearrayfact](xref:Microsoft.Quantum.Arrays.SquareArrayFact)
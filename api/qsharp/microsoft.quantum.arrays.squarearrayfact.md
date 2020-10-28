---
uid: Microsoft.Quantum.Arrays.SquareArrayFact
title: Squarearrayfact-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SquareArrayFact
qsharp.summary: Represents a condition that a 2-dimensional array has a square shape
ms.openlocfilehash: f7f0573db9098feebfd481624e11119c58fd9eed
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705767"
---
# <a name="squarearrayfact-function"></a>Squarearrayfact-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paketen [](https://nuget.org/packages/)


Stellt eine Bedingung dar, dass ein zweidimensionales Array über eine quadratische Form verfügt.

```qsharp
function SquareArrayFact<'T> (array : 'T[][], message : String) : Unit
```


## <a name="description"></a>BESCHREIBUNG

Diese Funktion bestätigt, dass jede Zeile in einem Array so viele Elemente aufweist, wie Zeilen (Elemente) im Array vorhanden sind.

## <a name="input"></a>Eingabe

### <a name="array--t"></a>Array: 't [] []

Ein zweidimensionales Array von-Elementen.


### <a name="message--string"></a>Message: [Zeichenfolge](xref:microsoft.quantum.lang-ref.string)

Eine Meldung, die gedruckt werden soll, wenn das Array kein quadratisches Array ist



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ der einzelnen Elemente von `array` .

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Arrays. rechgulararrayfact](xref:Microsoft.Quantum.Arrays.RectangularArrayFact)
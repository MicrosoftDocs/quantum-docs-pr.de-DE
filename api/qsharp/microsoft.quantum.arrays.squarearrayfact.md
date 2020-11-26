---
uid: Microsoft.Quantum.Arrays.SquareArrayFact
title: Squarearrayfact-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SquareArrayFact
qsharp.summary: Represents a condition that a 2-dimensional array has a square shape
ms.openlocfilehash: 3529718f0c903266d21fd593c11c0149dae0fa2c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220194"
---
# <a name="squarearrayfact-function"></a>Squarearrayfact-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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
---
uid: Microsoft.Quantum.Arrays.Diagonal
title: Diagonal-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Diagonal
qsharp.summary: Returns an array of diagonal elements of a 2-dimensional array
ms.openlocfilehash: 180b7185c94d712fa02100cb97abfbb6c464d12a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706119"
---
# <a name="diagonal-function"></a>Diagonal-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paketen [](https://nuget.org/packages/)


Gibt ein Array von diagonalen Elementen eines zweidimensionalen Arrays zurück.

```qsharp
function Diagonal<'T> (matrix : 'T[][]) : 'T[]
```


## <a name="description"></a>BESCHREIBUNG

Wenn das zweidimensionale Array keine quadratische Form aufweist, wird die Diagonale über dem Minimalwert über der Anzahl von Zeilen und Spalten zurückgegeben.

## <a name="input"></a>Eingabe

### <a name="matrix--t"></a>Matrix: 't [] []

zweidimensionale Matrix in Zeilen weiser Reihenfolge



## <a name="output--t"></a>Ausgabe: 't []



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ der einzelnen Elemente von `matrix` .

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Arrays. transferi](xref:Microsoft.Quantum.Arrays.Transposed)
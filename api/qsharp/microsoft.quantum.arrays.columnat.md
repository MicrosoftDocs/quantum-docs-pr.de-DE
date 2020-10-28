---
uid: Microsoft.Quantum.Arrays.ColumnAt
title: Columnat-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ColumnAt
qsharp.summary: Extracts a column from a matrix.
ms.openlocfilehash: ad09ada1a2253a54e70dddd6dba8aa243d2cd5a6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706167"
---
# <a name="columnat-function"></a>Columnat-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paketen [](https://nuget.org/packages/)


Extrahiert eine Spalte aus einer Matrix.

```qsharp
function ColumnAt<'T> (column : Int, matrix : 'T[][]) : 'T[]
```


## <a name="description"></a>BESCHREIBUNG

Diese Funktion extrahiert eine Spalte in einer Matrix in Zeilen weiser Reihenfolge.
Extrahieren einer Zeile ("corrsponds") für den Element Zugriff auf den ersten Index und erfordert daher keine weitere Behandlung.

## <a name="input"></a>Eingabe

### <a name="column--int"></a>Spalte: [int](xref:microsoft.quantum.lang-ref.int)

Spalte der Matrix


### <a name="matrix--t"></a>Matrix: 't [] []

zweidimensionale Matrix in Zeilen weiser Reihenfolge



## <a name="output--t"></a>Ausgabe: 't []



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ der einzelnen Elemente von `matrix` .

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Arrays. transferi](xref:Microsoft.Quantum.Arrays.Transposed)
- [Microsoft. Quantum. Arrays. Diagonal](xref:Microsoft.Quantum.Arrays.Diagonal)
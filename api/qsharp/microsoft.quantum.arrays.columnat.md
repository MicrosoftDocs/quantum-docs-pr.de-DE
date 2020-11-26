---
uid: Microsoft.Quantum.Arrays.ColumnAt
title: Columnat-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ColumnAt
qsharp.summary: Extracts a column from a matrix.
ms.openlocfilehash: 097b3fdd6fc1843ada27052fcf08ee80d894d25a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210097"
---
# <a name="columnat-function"></a>Columnat-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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
---
uid: Microsoft.Quantum.Arrays.Diagonal
title: Diagonal-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Diagonal
qsharp.summary: Returns an array of diagonal elements of a 2-dimensional array
ms.openlocfilehash: 2857046f59a958fed106af0944b75baaa3292e96
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842823"
---
# <a name="diagonal-function"></a>Diagonal-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt ein Array von diagonalen Elementen eines zweidimensionalen Arrays zurück.

```qsharp
function Diagonal<'T> (matrix : 'T[][]) : 'T[]
```


## <a name="description"></a>Beschreibung

Wenn das zweidimensionale Array keine quadratische Form aufweist, wird die Diagonale über dem Minimalwert über der Anzahl von Zeilen und Spalten zurückgegeben.

## <a name="input"></a>Eingabe

### <a name="matrix--t"></a>Matrix: 't [] []

zweidimensionale Matrix in Zeilen weiser Reihenfolge



## <a name="output--t"></a>Ausgabe: 't []



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ der einzelnen Elemente von `matrix` .

## <a name="example"></a>Beispiel

```qsharp
let matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]];
let diagonal = Diagonal(matrix);
// same as: column = [1, 5, 9]
```

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Arrays. transferi](xref:Microsoft.Quantum.Arrays.Transposed)
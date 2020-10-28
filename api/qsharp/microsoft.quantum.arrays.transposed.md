---
uid: Microsoft.Quantum.Arrays.Transposed
title: Funktion wurde umgesetzt
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Transposed
qsharp.summary: Returns the transpose of a matrix represented as an array of arrays.
ms.openlocfilehash: 54071c461cf9f9411c332763b81e3bc448fb6c6e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705738"
---
# <a name="transposed-function"></a>Funktion wurde umgesetzt

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paketen [](https://nuget.org/packages/)


Gibt das umsetzen einer Matrix zurück, die als Array von Arrays dargestellt wird.

```qsharp
function Transposed<'T> (matrix : 'T[][]) : 'T[][]
```


## <a name="description"></a>BESCHREIBUNG

Eingabe als $r \times c $ Matrix mit $r $ Rows und $c $ Columns.  Die Matrix ist zeilenbasiert, d. h., es wird `matrix[i][j]` auf das Element in Zeile $i $ und Spalte $j $ zugegriffen.

Diese Funktion gibt die $c \times r $-Matrix zurück, die das umsetzen der Eingabe Matrix ist.

## <a name="input"></a>Eingabe

### <a name="matrix--t"></a>Matrix: 't [] []

Zeilen basiertes $r \times c $ Matrix



## <a name="output--t"></a>Ausgabe: 't [] []

Umgesetzte $c \times r $ Matrix

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ der einzelnen Elemente von `matrix` .
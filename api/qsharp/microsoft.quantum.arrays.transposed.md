---
uid: Microsoft.Quantum.Arrays.Transposed
title: Funktion wurde umgesetzt
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Transposed
qsharp.summary: Returns the transpose of a matrix represented as an array of arrays.
ms.openlocfilehash: f293399d8e3a2cb32b2929e8d1591ac5eaefd277
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219990"
---
# <a name="transposed-function"></a>Funktion wurde umgesetzt

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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
---
uid: Microsoft.Quantum.Arrays.Flattened
title: Vereinfachte Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Flattened
qsharp.summary: Given an array of arrays, returns the concatenation of all arrays.
ms.openlocfilehash: 272533d4efd8598b21daa341c867c070a2083ce0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848619"
---
# <a name="flattened-function"></a>Vereinfachte Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt ein Array von Arrays zurück, das die Verkettung aller Arrays zurückgibt.

```qsharp
function Flattened<'T> (arrays : 'T[][]) : 'T[]
```


## <a name="input"></a>Eingabe

### <a name="arrays--t"></a>Arrays: 't [] []

Array von Arrays.



## <a name="output--t"></a>Ausgabe: 't []

Verkettung aller Arrays.

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ der `array` Elemente.

## <a name="example"></a>Beispiel

```qsharp
let flattened = Flattened([[1, 2], [3], [4, 5, 6]]);
// flattened = [1, 2, 3, 4, 5, 6]
```
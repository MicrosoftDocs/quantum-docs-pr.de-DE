---
uid: Microsoft.Quantum.Arrays.Interleaved
title: Interleaved-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Interleaved
qsharp.summary: Interleaves two arrays of (almost) same size.
ms.openlocfilehash: 1ff5999cc19f47e3dcae601b960446923b613d90
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220959"
---
# <a name="interleaved-function"></a>Interleaved-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Interverlässt zwei Arrays von (fast) gleicher Größe.

```qsharp
function Interleaved<'T> (first : 'T[], second : 'T[]) : 'T[]
```


## <a name="description"></a>BESCHREIBUNG

Diese Funktion gibt die überlappenden von zwei Arrays zurück, beginnend mit dem ersten Element aus dem ersten Array, dann mit dem ersten Element aus dem zweiten Array usw.

Das erste Array muss entweder dieselbe Länge wie das zweite Array aufweisen, oder es kann ein einziges Element aufweisen.

## <a name="input"></a>Eingabe

### <a name="first--t"></a>zuerst: 't []

Das erste zu verschachtelende Array.


### <a name="second--t"></a>Sekunde: 't []

Das zweite Array, das verschachtelt werden soll.



## <a name="output--t"></a>Ausgabe: 't []

Verschachtelte Arrays

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ der einzelnen Elemente von `first` und `second` .
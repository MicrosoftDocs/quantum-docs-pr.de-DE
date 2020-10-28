---
uid: Microsoft.Quantum.Arrays.Interleaved
title: Interleaved-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Interleaved
qsharp.summary: Interleaves two arrays of (almost) same size.
ms.openlocfilehash: 8405cabca17f2dd7c2680833bfab5c3768fcf752
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705959"
---
# <a name="interleaved-function"></a>Interleaved-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paketen [](https://nuget.org/packages/)


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
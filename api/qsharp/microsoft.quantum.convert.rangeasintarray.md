---
uid: Microsoft.Quantum.Convert.RangeAsIntArray
title: Rangeasintarray-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: RangeAsIntArray
qsharp.summary: Creates an array `arr` of integers enumerated by start..step..end.
ms.openlocfilehash: bd3ac51d2925d7a4450b2bc5e6f7899fcab18f2c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702923"
---
# <a name="rangeasintarray-function"></a>Rangeasintarray-Funktion

Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)

Paketen [](https://nuget.org/packages/)


Erstellt ein Array von ganzen Zahlen, die `arr` nach Start. aufgelistet sind. Schritt. Schließlich.

```qsharp
function RangeAsIntArray (range : Range) : Int[]
```


## <a name="input"></a>Eingabe

### <a name="range--range"></a>Bereich: [Bereich](xref:microsoft.quantum.lang-ref.range)

Eine `Range` von Werten `start..step..end` , die in ein Array konvertiert werden sollen.



## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)[]

Ein neues Array von ganzen Zahlen, das den Werten entspricht, die durch durchlaufen werden `range` .
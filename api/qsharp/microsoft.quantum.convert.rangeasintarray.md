---
uid: Microsoft.Quantum.Convert.RangeAsIntArray
title: Rangeasintarray-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: RangeAsIntArray
qsharp.summary: Creates an array `arr` of integers enumerated by start..step..end.
ms.openlocfilehash: f756e42aef7dc600e1fc6943a02513ac791f2320
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96214006"
---
# <a name="rangeasintarray-function"></a>Rangeasintarray-Funktion

Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Erstellt ein Array von ganzen Zahlen, die `arr` nach Start. aufgelistet sind. Schritt. Schließlich.

```qsharp
function RangeAsIntArray (range : Range) : Int[]
```


## <a name="input"></a>Eingabe

### <a name="range--range"></a>Bereich: [Bereich](xref:microsoft.quantum.lang-ref.range)

Eine `Range` von Werten `start..step..end` , die in ein Array konvertiert werden sollen.



## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)[]

Ein neues Array von ganzen Zahlen, das den Werten entspricht, die durch durchlaufen werden `range` .
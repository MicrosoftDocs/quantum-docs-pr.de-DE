---
uid: Microsoft.Quantum.Convert.RangeAsIntArray
title: Rangeasintarray-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: RangeAsIntArray
qsharp.summary: Creates an array `arr` of integers enumerated by start..step..end.
ms.openlocfilehash: 8c6b83d78e3b22ea1a17a48de66592950bf905a3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850099"
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

## <a name="example"></a>Beispiel

```qsharp
// The following returns [1,3,5,7];
let array = RangeAsIntArray(1..2..8);
```
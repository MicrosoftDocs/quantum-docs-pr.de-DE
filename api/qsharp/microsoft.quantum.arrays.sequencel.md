---
uid: Microsoft.Quantum.Arrays.SequenceL
title: Sequencel-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SequenceL
qsharp.summary: Get an array of integers in a given interval.
ms.openlocfilehash: 3e5c7f64825f09d82792d3e46fe3f53f5814510b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220262"
---
# <a name="sequencel-function"></a>Sequencel-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Ein Array von ganzen Zahlen in einem angegebenen Intervall erhalten.

```qsharp
function SequenceL (from : BigInt, to : BigInt) : BigInt[]
```


## <a name="input"></a>Eingabe

### <a name="from--bigint"></a>von: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Ein inklusiver Start Index des Intervalls.


### <a name="to--bigint"></a>an: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Ein inklusiver Endindex des Intervalls, das nicht kleiner als ist `from` .



## <a name="output--bigint"></a>Ausgabe: [bigint](xref:microsoft.quantum.lang-ref.bigint)[]

Ein Array, das die Reihenfolge der Zahlen `from` , `from + 1` ,..., enthält `to` .

## <a name="remarks"></a>Bemerkungen

Der Unterschied zwischen `from` und `to` muss in einen- `Int` Wert passen.
---
uid: Microsoft.Quantum.Arrays.SequenceL
title: Sequencel-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SequenceL
qsharp.summary: Get an array of integers in a given interval.
ms.openlocfilehash: d5ce63575e703341fce42c0be393765c342bbd89
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705783"
---
# <a name="sequencel-function"></a>Sequencel-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paketen [](https://nuget.org/packages/)


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

## <a name="remarks"></a>Hinweise

Der Unterschied zwischen `from` und `to` muss in einen- `Int` Wert passen.
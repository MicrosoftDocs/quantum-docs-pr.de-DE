---
uid: Microsoft.Quantum.Arrays.SequenceI
title: Sequencei-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SequenceI
qsharp.summary: Get an array of integers in a given interval.
ms.openlocfilehash: 5f03e5f2baff8077c1fa3fb5f1f079528ef0e215
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220296"
---
# <a name="sequencei-function"></a>Sequencei-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Ein Array von ganzen Zahlen in einem angegebenen Intervall erhalten.

```qsharp
function SequenceI (from : Int, to : Int) : Int[]
```


## <a name="input"></a>Eingabe

### <a name="from--int"></a>von: [int](xref:microsoft.quantum.lang-ref.int)

Ein inklusiver Start Index des Intervalls.


### <a name="to--int"></a>zu: [int](xref:microsoft.quantum.lang-ref.int)

Ein inklusiver Endindex des Intervalls, das nicht kleiner als ist `from` .



## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)[]

Ein Array, das die Reihenfolge der Zahlen `from` , `from + 1` ,..., enthält `to` .
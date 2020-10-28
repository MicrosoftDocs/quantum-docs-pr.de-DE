---
uid: Microsoft.Quantum.Arrays.SequenceI
title: Sequencei-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SequenceI
qsharp.summary: Get an array of integers in a given interval.
ms.openlocfilehash: d5dc4377c696e14b505c63701c2f5ca0dadca672
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705794"
---
# <a name="sequencei-function"></a>Sequencei-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paketen [](https://nuget.org/packages/)


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
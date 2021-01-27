---
uid: Microsoft.Quantum.Arrays.SequenceI
title: Sequencei-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SequenceI
qsharp.summary: Get an array of integers in a given interval.
ms.openlocfilehash: 3cf09e48cce1aeb1aac837465ee3a5e06adf5169
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851004"
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

## <a name="example"></a>Beispiel

```qsharp
let arr1 = SequenceI(0, 3); // [0, 1, 2, 3]
let arr2 = SequenceI(23, 29); // [23, 24, 25, 26, 27, 28, 29]
let arr3 = SequenceI(-5, -2); // [-5, -4, -3, -2]

let numbers = SequenceI(0, _); // function to create sequence from 0 to `to`
let naturals = SequenceI(1, _); // function to create sequence from 1 to `to`
```
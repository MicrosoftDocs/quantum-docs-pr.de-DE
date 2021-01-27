---
uid: Microsoft.Quantum.Arrays.Chunks
title: Blöcke (Funktion)
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Chunks
qsharp.summary: Splits an array into multiple parts of equal length.
ms.openlocfilehash: 977594839a7d2fe09de8138d32a4a50e8a752390
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842871"
---
# <a name="chunks-function"></a>Blöcke (Funktion)

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Teilt ein Array in mehrere Teile der gleichen Länge.

```qsharp
function Chunks<'T> (nElements : Int, arr : 'T[]) : 'T[][]
```


## <a name="input"></a>Eingabe

### <a name="nelements--int"></a>nelements: [int](xref:microsoft.quantum.lang-ref.int)

Die Länge der einzelnen Segmente.


### <a name="arr--t"></a>Arr: 't []

Das Array, das aufgeteilt werden soll.



## <a name="output--t"></a>Ausgabe: 't [] []

Ein-Array, das die einzelnen Segmente des ursprünglichen Arrays enthält.

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF



## <a name="remarks"></a>Bemerkungen

Beachten Sie, dass das letzte Element der Ausgabe möglicherweise kürzer `nElements` ist, als wenn `Length(arr)` von nicht teilbar ist `nElements` .
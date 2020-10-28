---
uid: Microsoft.Quantum.Arrays.Chunks
title: Blöcke (Funktion)
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Chunks
qsharp.summary: Splits an array into multiple parts of equal length.
ms.openlocfilehash: fe10999d35ed05908fd59b9dad8b5c0c51233ae6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706175"
---
# <a name="chunks-function"></a>Blöcke (Funktion)

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paketen [](https://nuget.org/packages/)


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



## <a name="remarks"></a>Hinweise

Beachten Sie, dass das letzte Element der Ausgabe möglicherweise kürzer `nElements` ist, als wenn `Length(arr)` von nicht teilbar ist `nElements` .
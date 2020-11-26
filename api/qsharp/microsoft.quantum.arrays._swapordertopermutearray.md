---
uid: Microsoft.Quantum.Arrays._SwapOrderToPermuteArray
title: _SwapOrderToPermuteArray-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: _SwapOrderToPermuteArray
qsharp.summary: Returns the order elements in an array need to be swapped to produce an ordered array. Assumes swaps occur in place.
ms.openlocfilehash: 9df2ec00d91c1124fae960efd15d576b15b0223c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221707"
---
# <a name="_swapordertopermutearray-function"></a>_SwapOrderToPermuteArray-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt die Reihenfolge Elemente in einem Array zurück, die ausgetauscht werden müssen, um ein geordnetes Array zu erzielen.
Setzt voraus, dass Austausch Vorgängen vorhanden sind.

```qsharp
function _SwapOrderToPermuteArray (newOrder : Int[]) : (Int, Int)[]
```


## <a name="input"></a>Eingabe

### <a name="neworder--int"></a>"nworder": [int](xref:microsoft.quantum.lang-ref.int)[]

Array mit der permutations der Indizes des neuen Arrays. Es sollten $n $-Elemente vorhanden sein, von denen jede eine eindeutige ganze Zahl zwischen $0 $ und $n-$1 ist.



## <a name="output--intint"></a>Ausgabe: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)) []

Das Tupel stellt die beiden Indizes dar, die ausgetauscht werden sollen. Die Austausch Vorgängen beginnen mit dem niedrigsten Index.

## <a name="remarks"></a>Bemerkungen

## <a name="psuedocode"></a>Psuedocode

for (Index in 0.. length (networder)-1) {while networder [index]! = Index {Switch networder [index] with networder [networder [index]]}}
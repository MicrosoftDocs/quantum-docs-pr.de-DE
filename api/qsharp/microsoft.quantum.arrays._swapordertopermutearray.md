---
uid: Microsoft.Quantum.Arrays._SwapOrderToPermuteArray
title: _SwapOrderToPermuteArray-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: _SwapOrderToPermuteArray
qsharp.summary: Returns the order elements in an array need to be swapped to produce an ordered array. Assumes swaps occur in place.
ms.openlocfilehash: 965f2f3d4f8b366abb27287ce0d27a3b7d7b8fb8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706191"
---
# <a name="_swapordertopermutearray-function"></a>_SwapOrderToPermuteArray-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paketen [](https://nuget.org/packages/)


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

## <a name="remarks"></a>Hinweise

## <a name="psuedocode"></a>Psuedocode

for (Index in 0.. length (networder)-1) {while networder [index]! = Index {Switch networder [index] with networder [networder [index]]}}
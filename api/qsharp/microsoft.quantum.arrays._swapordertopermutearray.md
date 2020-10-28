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
# <a name="_swapordertopermutearray-function"></a><span data-ttu-id="25d30-102">_SwapOrderToPermuteArray-Funktion</span><span class="sxs-lookup"><span data-stu-id="25d30-102">_SwapOrderToPermuteArray function</span></span>

<span data-ttu-id="25d30-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="25d30-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="25d30-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="25d30-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="25d30-105">Gibt die Reihenfolge Elemente in einem Array zurück, die ausgetauscht werden müssen, um ein geordnetes Array zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="25d30-105">Returns the order elements in an array need to be swapped to produce an ordered array.</span></span>
<span data-ttu-id="25d30-106">Setzt voraus, dass Austausch Vorgängen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="25d30-106">Assumes swaps occur in place.</span></span>

```qsharp
function _SwapOrderToPermuteArray (newOrder : Int[]) : (Int, Int)[]
```


## <a name="input"></a><span data-ttu-id="25d30-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="25d30-107">Input</span></span>

### <a name="neworder--int"></a><span data-ttu-id="25d30-108">"nworder": [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="25d30-108">newOrder : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="25d30-109">Array mit der permutations der Indizes des neuen Arrays.</span><span class="sxs-lookup"><span data-stu-id="25d30-109">Array with the permutation of the indices of the new array.</span></span> <span data-ttu-id="25d30-110">Es sollten $n $-Elemente vorhanden sein, von denen jede eine eindeutige ganze Zahl zwischen $0 $ und $n-$1 ist.</span><span class="sxs-lookup"><span data-stu-id="25d30-110">There should be $n$ elements, each being a unique integer from $0$ to $n-1$.</span></span>



## <a name="output--intint"></a><span data-ttu-id="25d30-111">Ausgabe: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)) []</span><span class="sxs-lookup"><span data-stu-id="25d30-111">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))[]</span></span>

<span data-ttu-id="25d30-112">Das Tupel stellt die beiden Indizes dar, die ausgetauscht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="25d30-112">The tuple represents the two indices to be swapped.</span></span> <span data-ttu-id="25d30-113">Die Austausch Vorgängen beginnen mit dem niedrigsten Index.</span><span class="sxs-lookup"><span data-stu-id="25d30-113">The swaps begin at the lowest index.</span></span>

## <a name="remarks"></a><span data-ttu-id="25d30-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="25d30-114">Remarks</span></span>

## <a name="psuedocode"></a><span data-ttu-id="25d30-115">Psuedocode</span><span class="sxs-lookup"><span data-stu-id="25d30-115">Psuedocode</span></span>

<span data-ttu-id="25d30-116">for (Index in 0.. length (networder)-1) {while networder [index]! = Index {Switch networder [index] with networder [networder [index]]}}</span><span class="sxs-lookup"><span data-stu-id="25d30-116">for (index in 0..Length(newOrder) - 1) { while newOrder[index] != index { Switch newOrder[index] with newOrder[newOrder[index]] } }</span></span>
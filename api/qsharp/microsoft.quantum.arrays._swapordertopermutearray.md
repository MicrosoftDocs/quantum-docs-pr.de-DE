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
# <a name="_swapordertopermutearray-function"></a><span data-ttu-id="67fb1-102">_SwapOrderToPermuteArray-Funktion</span><span class="sxs-lookup"><span data-stu-id="67fb1-102">_SwapOrderToPermuteArray function</span></span>

<span data-ttu-id="67fb1-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="67fb1-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="67fb1-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="67fb1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="67fb1-105">Gibt die Reihenfolge Elemente in einem Array zurück, die ausgetauscht werden müssen, um ein geordnetes Array zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="67fb1-105">Returns the order elements in an array need to be swapped to produce an ordered array.</span></span>
<span data-ttu-id="67fb1-106">Setzt voraus, dass Austausch Vorgängen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="67fb1-106">Assumes swaps occur in place.</span></span>

```qsharp
function _SwapOrderToPermuteArray (newOrder : Int[]) : (Int, Int)[]
```


## <a name="input"></a><span data-ttu-id="67fb1-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="67fb1-107">Input</span></span>

### <a name="neworder--int"></a><span data-ttu-id="67fb1-108">"nworder": [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="67fb1-108">newOrder : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="67fb1-109">Array mit der permutations der Indizes des neuen Arrays.</span><span class="sxs-lookup"><span data-stu-id="67fb1-109">Array with the permutation of the indices of the new array.</span></span> <span data-ttu-id="67fb1-110">Es sollten $n $-Elemente vorhanden sein, von denen jede eine eindeutige ganze Zahl zwischen $0 $ und $n-$1 ist.</span><span class="sxs-lookup"><span data-stu-id="67fb1-110">There should be $n$ elements, each being a unique integer from $0$ to $n-1$.</span></span>



## <a name="output--intint"></a><span data-ttu-id="67fb1-111">Ausgabe: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)) []</span><span class="sxs-lookup"><span data-stu-id="67fb1-111">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))[]</span></span>

<span data-ttu-id="67fb1-112">Das Tupel stellt die beiden Indizes dar, die ausgetauscht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="67fb1-112">The tuple represents the two indices to be swapped.</span></span> <span data-ttu-id="67fb1-113">Die Austausch Vorgängen beginnen mit dem niedrigsten Index.</span><span class="sxs-lookup"><span data-stu-id="67fb1-113">The swaps begin at the lowest index.</span></span>

## <a name="remarks"></a><span data-ttu-id="67fb1-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="67fb1-114">Remarks</span></span>

## <a name="psuedocode"></a><span data-ttu-id="67fb1-115">Psuedocode</span><span class="sxs-lookup"><span data-stu-id="67fb1-115">Psuedocode</span></span>

<span data-ttu-id="67fb1-116">for (Index in 0.. length (networder)-1) {while networder [index]! = Index {Switch networder [index] with networder [networder [index]]}}</span><span class="sxs-lookup"><span data-stu-id="67fb1-116">for (index in 0..Length(newOrder) - 1) { while newOrder[index] != index { Switch newOrder[index] with newOrder[newOrder[index]] } }</span></span>
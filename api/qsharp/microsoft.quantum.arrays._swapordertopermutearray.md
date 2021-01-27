---
uid: Microsoft.Quantum.Arrays._SwapOrderToPermuteArray
title: _SwapOrderToPermuteArray-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: _SwapOrderToPermuteArray
qsharp.summary: Returns the order elements in an array need to be swapped to produce an ordered array. Assumes swaps occur in place.
ms.openlocfilehash: ff8e4e23dde7d69f93054a275548ded49d5b0bfb
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846290"
---
# <a name="_swapordertopermutearray-function"></a><span data-ttu-id="cfc82-102">_SwapOrderToPermuteArray-Funktion</span><span class="sxs-lookup"><span data-stu-id="cfc82-102">_SwapOrderToPermuteArray function</span></span>

<span data-ttu-id="cfc82-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="cfc82-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="cfc82-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cfc82-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cfc82-105">Gibt die Reihenfolge Elemente in einem Array zurück, die ausgetauscht werden müssen, um ein geordnetes Array zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="cfc82-105">Returns the order elements in an array need to be swapped to produce an ordered array.</span></span>
<span data-ttu-id="cfc82-106">Setzt voraus, dass Austausch Vorgängen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="cfc82-106">Assumes swaps occur in place.</span></span>

```qsharp
function _SwapOrderToPermuteArray (newOrder : Int[]) : (Int, Int)[]
```


## <a name="input"></a><span data-ttu-id="cfc82-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cfc82-107">Input</span></span>

### <a name="neworder--int"></a><span data-ttu-id="cfc82-108">"nworder": [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="cfc82-108">newOrder : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="cfc82-109">Array mit der permutations der Indizes des neuen Arrays.</span><span class="sxs-lookup"><span data-stu-id="cfc82-109">Array with the permutation of the indices of the new array.</span></span> <span data-ttu-id="cfc82-110">Es sollten $n $-Elemente vorhanden sein, von denen jede eine eindeutige ganze Zahl zwischen $0 $ und $n-$1 ist.</span><span class="sxs-lookup"><span data-stu-id="cfc82-110">There should be $n$ elements, each being a unique integer from $0$ to $n-1$.</span></span>



## <a name="output--intint"></a><span data-ttu-id="cfc82-111">Ausgabe: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)) []</span><span class="sxs-lookup"><span data-stu-id="cfc82-111">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))[]</span></span>

<span data-ttu-id="cfc82-112">Das Tupel stellt die beiden Indizes dar, die ausgetauscht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cfc82-112">The tuple represents the two indices to be swapped.</span></span> <span data-ttu-id="cfc82-113">Die Austausch Vorgängen beginnen mit dem niedrigsten Index.</span><span class="sxs-lookup"><span data-stu-id="cfc82-113">The swaps begin at the lowest index.</span></span>

## <a name="example"></a><span data-ttu-id="cfc82-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="cfc82-114">Example</span></span>

```qsharp
// The following returns [(0, 5),(0, 4),(0, 1),(0, 3)];
let swapOrder = _SwapOrderToPermuteArray([5, 3, 2, 0, 1, 4]);
```

## <a name="remarks"></a><span data-ttu-id="cfc82-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cfc82-115">Remarks</span></span>

## <a name="psuedocode"></a><span data-ttu-id="cfc82-116">Psuedocode</span><span class="sxs-lookup"><span data-stu-id="cfc82-116">Psuedocode</span></span>

<span data-ttu-id="cfc82-117">for (Index in 0.. length (networder)-1) {while networder [index]! = Index {Switch networder [index] with networder [networder [index]]}}</span><span class="sxs-lookup"><span data-stu-id="cfc82-117">for (index in 0..Length(newOrder) - 1) { while newOrder[index] != index { Switch newOrder[index] with newOrder[newOrder[index]] } }</span></span>
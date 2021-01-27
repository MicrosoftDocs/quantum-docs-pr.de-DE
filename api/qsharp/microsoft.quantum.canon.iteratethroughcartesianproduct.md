---
uid: Microsoft.Quantum.Canon.IterateThroughCartesianProduct
title: Iteratethrough cartesianproduct-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IterateThroughCartesianProduct
qsharp.summary: Applies an operation for each index in the Cartesian product of several ranges.
ms.openlocfilehash: a0aaa8ef6aa6798d31c810254c92820f8136800c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840278"
---
# <a name="iteratethroughcartesianproduct-operation"></a><span data-ttu-id="561b7-102">Iteratethrough cartesianproduct-Vorgang</span><span class="sxs-lookup"><span data-stu-id="561b7-102">IterateThroughCartesianProduct operation</span></span>

<span data-ttu-id="561b7-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="561b7-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="561b7-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="561b7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="561b7-105">Wendet einen Vorgang für jeden Index im kartesischen Produkt mehrerer Bereiche an.</span><span class="sxs-lookup"><span data-stu-id="561b7-105">Applies an operation for each index in the Cartesian product of several ranges.</span></span>

```qsharp
operation IterateThroughCartesianProduct (bounds : Int[], op : (Int[] => Unit)) : Unit
```


## <a name="description"></a><span data-ttu-id="561b7-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="561b7-106">Description</span></span>

<span data-ttu-id="561b7-107">Wendet iterativ einen Vorgang für jedes Element des kartesischen Produkts von `0..(bounds[0] - 1)` , `0..(bounds[1] - 1)` ,... an, `0..(bounds[Length(bounds) - 1] - 1)`</span><span class="sxs-lookup"><span data-stu-id="561b7-107">Iteratively applies an operation for each element of the Cartesian product of `0..(bounds[0] - 1)`, `0..(bounds[1] - 1)`, ..., `0..(bounds[Length(bounds) - 1] - 1)`</span></span>

## <a name="input"></a><span data-ttu-id="561b7-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="561b7-108">Input</span></span>

### <a name="bounds--int"></a><span data-ttu-id="561b7-109">Begrenzungen: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="561b7-109">bounds : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="561b7-110">Ein Array, das die Bereiche angibt, die durchlaufen werden sollen, wobei jeder Bereich als ganzzahlige Länge angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="561b7-110">An array specifying the ranges to be iterated over, with each range being specified as an integer length.</span></span>


### <a name="op--int--unit"></a><span data-ttu-id="561b7-111">OP: [int](xref:microsoft.quantum.lang-ref.int)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="561b7-111">op : [Int](xref:microsoft.quantum.lang-ref.int)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="561b7-112">Ein Vorgang, der für jedes Element des angegebenen kartesischen Produkts aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="561b7-112">An operation to be called for each element of the given Cartesian product.</span></span>



## <a name="output--unit"></a><span data-ttu-id="561b7-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="561b7-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="561b7-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="561b7-114">Example</span></span>

<span data-ttu-id="561b7-115">Bei einem Vorgang `op` sind die folgenden beiden Code Ausschnitte äquivalent:</span><span class="sxs-lookup"><span data-stu-id="561b7-115">Given an operation `op`, the following two snippets are equivalent:</span></span>

```qsharp
IterateThroughCartesianProduct([3, 4, 5], op);
```

```qsharp
op([0, 0, 0]);
op([1, 0, 0]);
op([2, 0, 0]);
op([0, 1, 0]);
// ...
op([0, 3, 0]);
op([0, 0, 1]);
//
op([2, 3, 4]);
```

## <a name="see-also"></a><span data-ttu-id="561b7-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="561b7-116">See Also</span></span>

- [<span data-ttu-id="561b7-117">Microsoft. Quantum. Canon. iteratequercartesianpower</span><span class="sxs-lookup"><span data-stu-id="561b7-117">Microsoft.Quantum.Canon.IterateThroughCartesianPower</span></span>](xref:Microsoft.Quantum.Canon.IterateThroughCartesianPower)
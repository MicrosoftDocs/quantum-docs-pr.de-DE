---
uid: Microsoft.Quantum.Canon.IterateThroughCartesianProduct
title: Iteratethrough cartesianproduct-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IterateThroughCartesianProduct
qsharp.summary: Applies an operation for each index in the Cartesian product of several ranges.
ms.openlocfilehash: 6340c7a972253e6f583a3856df93a7066ced3139
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96206441"
---
# <a name="iteratethroughcartesianproduct-operation"></a><span data-ttu-id="74640-102">Iteratethrough cartesianproduct-Vorgang</span><span class="sxs-lookup"><span data-stu-id="74640-102">IterateThroughCartesianProduct operation</span></span>

<span data-ttu-id="74640-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="74640-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="74640-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="74640-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="74640-105">Wendet einen Vorgang für jeden Index im kartesischen Produkt mehrerer Bereiche an.</span><span class="sxs-lookup"><span data-stu-id="74640-105">Applies an operation for each index in the Cartesian product of several ranges.</span></span>

```qsharp
operation IterateThroughCartesianProduct (bounds : Int[], op : (Int[] => Unit)) : Unit
```


## <a name="description"></a><span data-ttu-id="74640-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="74640-106">Description</span></span>

<span data-ttu-id="74640-107">Wendet iterativ einen Vorgang für jedes Element des kartesischen Produkts von `0..(bounds[0] - 1)` , `0..(bounds[1] - 1)` ,... an, `0..(bounds[Length(bounds) - 1] - 1)`</span><span class="sxs-lookup"><span data-stu-id="74640-107">Iteratively applies an operation for each element of the Cartesian product of `0..(bounds[0] - 1)`, `0..(bounds[1] - 1)`, ..., `0..(bounds[Length(bounds) - 1] - 1)`</span></span>

## <a name="input"></a><span data-ttu-id="74640-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="74640-108">Input</span></span>

### <a name="bounds--int"></a><span data-ttu-id="74640-109">Begrenzungen: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="74640-109">bounds : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="74640-110">Ein Array, das die Bereiche angibt, die durchlaufen werden sollen, wobei jeder Bereich als ganzzahlige Länge angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="74640-110">An array specifying the ranges to be iterated over, with each range being specified as an integer length.</span></span>


### <a name="op--int--unit"></a><span data-ttu-id="74640-111">OP: [int](xref:microsoft.quantum.lang-ref.int)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="74640-111">op : [Int](xref:microsoft.quantum.lang-ref.int)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="74640-112">Ein Vorgang, der für jedes Element des angegebenen kartesischen Produkts aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="74640-112">An operation to be called for each element of the given Cartesian product.</span></span>



## <a name="output--unit"></a><span data-ttu-id="74640-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="74640-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="74640-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="74640-114">See Also</span></span>

- [<span data-ttu-id="74640-115">Microsoft. Quantum. Canon. iteratequercartesianpower</span><span class="sxs-lookup"><span data-stu-id="74640-115">Microsoft.Quantum.Canon.IterateThroughCartesianPower</span></span>](xref:Microsoft.Quantum.Canon.IterateThroughCartesianPower)
---
uid: Microsoft.Quantum.Canon.IterateThroughCartesianPower
title: Iteratethrough cartesianpower-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IterateThroughCartesianPower
qsharp.summary: Applies an operation for each index in the Cartesian power of an integer range.
ms.openlocfilehash: 2883e7cb30633afe51d380befe806665207c5abd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96206475"
---
# <a name="iteratethroughcartesianpower-operation"></a><span data-ttu-id="8f3b3-102">Iteratethrough cartesianpower-Vorgang</span><span class="sxs-lookup"><span data-stu-id="8f3b3-102">IterateThroughCartesianPower operation</span></span>

<span data-ttu-id="8f3b3-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="8f3b3-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="8f3b3-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8f3b3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8f3b3-105">Wendet einen Vorgang für jeden Index in der kartesischen Potenz eines ganzzahligen Bereichs an.</span><span class="sxs-lookup"><span data-stu-id="8f3b3-105">Applies an operation for each index in the Cartesian power of an integer range.</span></span>

```qsharp
operation IterateThroughCartesianPower (power : Int, bound : Int, op : (Int[] => Unit)) : Unit
```


## <a name="description"></a><span data-ttu-id="8f3b3-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8f3b3-106">Description</span></span>

<span data-ttu-id="8f3b3-107">Wendet iterativ einen Vorgang für jedes Element einer kartesischen Potenz des Bereichs an `0..(bound - 1)` .</span><span class="sxs-lookup"><span data-stu-id="8f3b3-107">Iteratively applies an operation for each element of a Cartesian power of the range `0..(bound - 1)`.</span></span>

## <a name="input"></a><span data-ttu-id="8f3b3-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8f3b3-108">Input</span></span>

### <a name="power--int"></a><span data-ttu-id="8f3b3-109">Power: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8f3b3-109">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="8f3b3-110">Die kartesische Potenz, in die der Bereich `0..(bound - 1)` ausgelöst werden soll.</span><span class="sxs-lookup"><span data-stu-id="8f3b3-110">The Cartesian power to which the range `0..(bound - 1)` should be raised.</span></span>


### <a name="bound--int"></a><span data-ttu-id="8f3b3-111">gebunden: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8f3b3-111">bound : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="8f3b3-112">Eine Spezifikation des Bereichs, der durchlaufen werden soll, angegeben als die Länge des Bereichs.</span><span class="sxs-lookup"><span data-stu-id="8f3b3-112">A specification of the range to be iterated over, given as the length of the range.</span></span>


### <a name="op--int--unit"></a><span data-ttu-id="8f3b3-113">OP: [int](xref:microsoft.quantum.lang-ref.int)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8f3b3-113">op : [Int](xref:microsoft.quantum.lang-ref.int)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="8f3b3-114">Ein Vorgang, der für jedes Element der angegebenen kartesischen Potenz aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="8f3b3-114">An operation to be called for each element of the given Cartesian power.</span></span>



## <a name="output--unit"></a><span data-ttu-id="8f3b3-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8f3b3-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="8f3b3-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8f3b3-116">See Also</span></span>

- [<span data-ttu-id="8f3b3-117">Microsoft. Quantum. Canon. iteratequercartesianproduct</span><span class="sxs-lookup"><span data-stu-id="8f3b3-117">Microsoft.Quantum.Canon.IterateThroughCartesianProduct</span></span>](xref:Microsoft.Quantum.Canon.IterateThroughCartesianProduct)
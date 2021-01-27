---
uid: Microsoft.Quantum.Canon.IterateThroughCartesianPower
title: Iteratethrough cartesianpower-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IterateThroughCartesianPower
qsharp.summary: Applies an operation for each index in the Cartesian power of an integer range.
ms.openlocfilehash: 3a303d13c4a6f102dab92d814e24df9d90213fbe
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840294"
---
# <a name="iteratethroughcartesianpower-operation"></a><span data-ttu-id="5ca9c-102">Iteratethrough cartesianpower-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5ca9c-102">IterateThroughCartesianPower operation</span></span>

<span data-ttu-id="5ca9c-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5ca9c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5ca9c-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5ca9c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5ca9c-105">Wendet einen Vorgang für jeden Index in der kartesischen Potenz eines ganzzahligen Bereichs an.</span><span class="sxs-lookup"><span data-stu-id="5ca9c-105">Applies an operation for each index in the Cartesian power of an integer range.</span></span>

```qsharp
operation IterateThroughCartesianPower (power : Int, bound : Int, op : (Int[] => Unit)) : Unit
```


## <a name="description"></a><span data-ttu-id="5ca9c-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5ca9c-106">Description</span></span>

<span data-ttu-id="5ca9c-107">Wendet iterativ einen Vorgang für jedes Element einer kartesischen Potenz des Bereichs an `0..(bound - 1)` .</span><span class="sxs-lookup"><span data-stu-id="5ca9c-107">Iteratively applies an operation for each element of a Cartesian power of the range `0..(bound - 1)`.</span></span>

## <a name="input"></a><span data-ttu-id="5ca9c-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5ca9c-108">Input</span></span>

### <a name="power--int"></a><span data-ttu-id="5ca9c-109">Power: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5ca9c-109">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5ca9c-110">Die kartesische Potenz, in die der Bereich `0..(bound - 1)` ausgelöst werden soll.</span><span class="sxs-lookup"><span data-stu-id="5ca9c-110">The Cartesian power to which the range `0..(bound - 1)` should be raised.</span></span>


### <a name="bound--int"></a><span data-ttu-id="5ca9c-111">gebunden: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5ca9c-111">bound : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5ca9c-112">Eine Spezifikation des Bereichs, der durchlaufen werden soll, angegeben als die Länge des Bereichs.</span><span class="sxs-lookup"><span data-stu-id="5ca9c-112">A specification of the range to be iterated over, given as the length of the range.</span></span>


### <a name="op--int--unit"></a><span data-ttu-id="5ca9c-113">OP: [int](xref:microsoft.quantum.lang-ref.int)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5ca9c-113">op : [Int](xref:microsoft.quantum.lang-ref.int)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="5ca9c-114">Ein Vorgang, der für jedes Element der angegebenen kartesischen Potenz aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5ca9c-114">An operation to be called for each element of the given Cartesian power.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5ca9c-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5ca9c-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="5ca9c-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5ca9c-116">Example</span></span>

<span data-ttu-id="5ca9c-117">Bei einem Vorgang `op` sind die folgenden beiden Code Ausschnitte äquivalent:</span><span class="sxs-lookup"><span data-stu-id="5ca9c-117">Given an operation `op`, the following two snippets are equivalent:</span></span>

```qsharp
IterateThroughCartesianPower(2, 3, op);
```

```qsharp
op([0, 0]);
op([1, 0]);
op([2, 0]);
op([0, 1]);
// ..
op([2, 2]);
```

## <a name="see-also"></a><span data-ttu-id="5ca9c-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5ca9c-118">See Also</span></span>

- [<span data-ttu-id="5ca9c-119">Microsoft. Quantum. Canon. iteratequercartesianproduct</span><span class="sxs-lookup"><span data-stu-id="5ca9c-119">Microsoft.Quantum.Canon.IterateThroughCartesianProduct</span></span>](xref:Microsoft.Quantum.Canon.IterateThroughCartesianProduct)
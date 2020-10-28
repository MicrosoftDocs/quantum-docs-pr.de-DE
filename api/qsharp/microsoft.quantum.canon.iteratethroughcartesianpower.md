---
uid: Microsoft.Quantum.Canon.IterateThroughCartesianPower
title: Iteratethrough cartesianpower-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IterateThroughCartesianPower
qsharp.summary: Applies an operation for each index in the Cartesian power of an integer range.
ms.openlocfilehash: 526d28cbf3cd356b4f48eec02b3f032f70a868d9
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704087"
---
# <a name="iteratethroughcartesianpower-operation"></a><span data-ttu-id="60c32-102">Iteratethrough cartesianpower-Vorgang</span><span class="sxs-lookup"><span data-stu-id="60c32-102">IterateThroughCartesianPower operation</span></span>

<span data-ttu-id="60c32-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="60c32-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="60c32-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="60c32-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="60c32-105">Wendet einen Vorgang für jeden Index in der kartesischen Potenz eines ganzzahligen Bereichs an.</span><span class="sxs-lookup"><span data-stu-id="60c32-105">Applies an operation for each index in the Cartesian power of an integer range.</span></span>

```qsharp
operation IterateThroughCartesianPower (power : Int, bound : Int, op : (Int[] => Unit)) : Unit
```


## <a name="description"></a><span data-ttu-id="60c32-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="60c32-106">Description</span></span>

<span data-ttu-id="60c32-107">Wendet iterativ einen Vorgang für jedes Element einer kartesischen Potenz des Bereichs an `0..(bound - 1)` .</span><span class="sxs-lookup"><span data-stu-id="60c32-107">Iteratively applies an operation for each element of a Cartesian power of the range `0..(bound - 1)`.</span></span>

## <a name="input"></a><span data-ttu-id="60c32-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="60c32-108">Input</span></span>

### <a name="power--int"></a><span data-ttu-id="60c32-109">Power: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="60c32-109">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="60c32-110">Die kartesische Potenz, in die der Bereich `0..(bound - 1)` ausgelöst werden soll.</span><span class="sxs-lookup"><span data-stu-id="60c32-110">The Cartesian power to which the range `0..(bound - 1)` should be raised.</span></span>


### <a name="bound--int"></a><span data-ttu-id="60c32-111">gebunden: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="60c32-111">bound : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="60c32-112">Eine Spezifikation des Bereichs, der durchlaufen werden soll, angegeben als die Länge des Bereichs.</span><span class="sxs-lookup"><span data-stu-id="60c32-112">A specification of the range to be iterated over, given as the length of the range.</span></span>


### <a name="op--int--unit"></a><span data-ttu-id="60c32-113">OP: [int](xref:microsoft.quantum.lang-ref.int)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="60c32-113">op : [Int](xref:microsoft.quantum.lang-ref.int)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="60c32-114">Ein Vorgang, der für jedes Element der angegebenen kartesischen Potenz aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="60c32-114">An operation to be called for each element of the given Cartesian power.</span></span>



## <a name="output--unit"></a><span data-ttu-id="60c32-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="60c32-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="60c32-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="60c32-116">See Also</span></span>

- [<span data-ttu-id="60c32-117">Microsoft. Quantum. Canon. iteratequercartesianproduct</span><span class="sxs-lookup"><span data-stu-id="60c32-117">Microsoft.Quantum.Canon.IterateThroughCartesianProduct</span></span>](xref:Microsoft.Quantum.Canon.IterateThroughCartesianProduct)
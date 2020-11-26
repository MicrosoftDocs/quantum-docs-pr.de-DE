---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOps
title: Applyseriesofops-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOps
qsharp.summary: Applies a list of ops and their targets sequentially on an array.
ms.openlocfilehash: b8810e7d31689046e72905195a3a25ef80fc8d67
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218001"
---
# <a name="applyseriesofops-operation"></a><span data-ttu-id="e9b02-102">Applyseriesofops-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e9b02-102">ApplySeriesOfOps operation</span></span>

<span data-ttu-id="e9b02-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e9b02-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e9b02-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e9b02-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e9b02-105">Wendet eine Liste von OPS und deren Zielen sequenziell auf ein Array an.</span><span class="sxs-lookup"><span data-stu-id="e9b02-105">Applies a list of ops and their targets sequentially on an array.</span></span>

```qsharp
operation ApplySeriesOfOps<'T> (listOfOps : ('T[] => Unit)[], targets : Int[][], register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="e9b02-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e9b02-106">Input</span></span>

### <a name="listofops--t--unit-"></a><span data-ttu-id="e9b02-107">listOf: 't [] => [Unit](xref:microsoft.quantum.lang-ref.unit) []</span><span class="sxs-lookup"><span data-stu-id="e9b02-107">listOfOps : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit) []</span></span>

<span data-ttu-id="e9b02-108">Die Liste der OPS, die jeweils ein nicht-Array enthalten, das angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9b02-108">List of ops, each taking a 'T array, to be applied.</span></span> <span data-ttu-id="e9b02-109">Sie werden sequenziell, der niedrigste Index zuerst angewendet.</span><span class="sxs-lookup"><span data-stu-id="e9b02-109">They are applied sequentially, lowest index first.</span></span>


### <a name="targets--int"></a><span data-ttu-id="e9b02-110">Ziele: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="e9b02-110">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="e9b02-111">Geschmestete Arrays, die die Ziele des OP beschreiben.</span><span class="sxs-lookup"><span data-stu-id="e9b02-111">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="e9b02-112">Jedes Array muss eine Liste von Punkten enthalten, in denen die zu verwendenden Indizes beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="e9b02-112">Each array should contain a list of ints describing the indices to be used.</span></span>


### <a name="register--t"></a><span data-ttu-id="e9b02-113">Register: 't []</span><span class="sxs-lookup"><span data-stu-id="e9b02-113">register : 'T[]</span></span>

<span data-ttu-id="e9b02-114">Das Qubit-Register, das bearbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9b02-114">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e9b02-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e9b02-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="e9b02-116">Typparameter</span><span class="sxs-lookup"><span data-stu-id="e9b02-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e9b02-117">GIF</span><span class="sxs-lookup"><span data-stu-id="e9b02-117">'T</span></span>



## <a name="see-also"></a><span data-ttu-id="e9b02-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e9b02-118">See Also</span></span>

- [<span data-ttu-id="e9b02-119">Microsoft. Quantum. Canon. applyoprepeatedlyover</span><span class="sxs-lookup"><span data-stu-id="e9b02-119">Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver</span></span>](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)
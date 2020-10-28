---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOps
title: Applyseriesofops-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOps
qsharp.summary: Applies a list of ops and their targets sequentially on an array.
ms.openlocfilehash: aff0bcb831960153166e88aef1f05e000125d5d8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705026"
---
# <a name="applyseriesofops-operation"></a><span data-ttu-id="484fa-102">Applyseriesofops-Vorgang</span><span class="sxs-lookup"><span data-stu-id="484fa-102">ApplySeriesOfOps operation</span></span>

<span data-ttu-id="484fa-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="484fa-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="484fa-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="484fa-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="484fa-105">Wendet eine Liste von OPS und deren Zielen sequenziell auf ein Array an.</span><span class="sxs-lookup"><span data-stu-id="484fa-105">Applies a list of ops and their targets sequentially on an array.</span></span>

```qsharp
operation ApplySeriesOfOps<'T> (listOfOps : ('T[] => Unit)[], targets : Int[][], register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="484fa-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="484fa-106">Input</span></span>

### <a name="listofops--t--unit-"></a><span data-ttu-id="484fa-107">listOf: 't [] => [Unit](xref:microsoft.quantum.lang-ref.unit) []</span><span class="sxs-lookup"><span data-stu-id="484fa-107">listOfOps : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit) []</span></span>

<span data-ttu-id="484fa-108">Die Liste der OPS, die jeweils ein nicht-Array enthalten, das angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="484fa-108">List of ops, each taking a 'T array, to be applied.</span></span> <span data-ttu-id="484fa-109">Sie werden sequenziell, der niedrigste Index zuerst angewendet.</span><span class="sxs-lookup"><span data-stu-id="484fa-109">They are applied sequentially, lowest index first.</span></span>


### <a name="targets--int"></a><span data-ttu-id="484fa-110">Ziele: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="484fa-110">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="484fa-111">Geschmestete Arrays, die die Ziele des OP beschreiben.</span><span class="sxs-lookup"><span data-stu-id="484fa-111">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="484fa-112">Jedes Array muss eine Liste von Punkten enthalten, in denen die zu verwendenden Indizes beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="484fa-112">Each array should contain a list of ints describing the indices to be used.</span></span>


### <a name="register--t"></a><span data-ttu-id="484fa-113">Register: 't []</span><span class="sxs-lookup"><span data-stu-id="484fa-113">register : 'T[]</span></span>

<span data-ttu-id="484fa-114">Das Qubit-Register, das bearbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="484fa-114">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="484fa-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="484fa-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="484fa-116">Typparameter</span><span class="sxs-lookup"><span data-stu-id="484fa-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="484fa-117">GIF</span><span class="sxs-lookup"><span data-stu-id="484fa-117">'T</span></span>



## <a name="see-also"></a><span data-ttu-id="484fa-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="484fa-118">See Also</span></span>

- [<span data-ttu-id="484fa-119">Microsoft. Quantum. Canon. applyoprepeatedlyover</span><span class="sxs-lookup"><span data-stu-id="484fa-119">Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver</span></span>](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)
---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOpsC
title: Applyseriesofopsc-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOpsC
qsharp.summary: Applies a list of ops and their targets sequentially on an array. (Controlled)
ms.openlocfilehash: d909aadbfe86f6d1314e9be5434249c40932ae4a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705015"
---
# <a name="applyseriesofopsc-operation"></a><span data-ttu-id="94b89-102">Applyseriesofopsc-Vorgang</span><span class="sxs-lookup"><span data-stu-id="94b89-102">ApplySeriesOfOpsC operation</span></span>

<span data-ttu-id="94b89-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="94b89-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="94b89-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="94b89-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="94b89-105">Wendet eine Liste von OPS und deren Zielen sequenziell auf ein Array an.</span><span class="sxs-lookup"><span data-stu-id="94b89-105">Applies a list of ops and their targets sequentially on an array.</span></span> <span data-ttu-id="94b89-106">Klimatisiert</span><span class="sxs-lookup"><span data-stu-id="94b89-106">(Controlled)</span></span>

```qsharp
operation ApplySeriesOfOpsC<'T> (listOfOps : ('T[] => Unit is Ctl)[], targets : Int[][], register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="94b89-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="94b89-107">Input</span></span>

### <a name="listofops--t--unit-ctl"></a><span data-ttu-id="94b89-108">listOf: 't [] => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL []</span><span class="sxs-lookup"><span data-stu-id="94b89-108">listOfOps : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl[]</span></span>

<span data-ttu-id="94b89-109">Die Liste der OPS, die jeweils ein nicht-Array enthalten, das angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="94b89-109">List of ops, each taking a 'T array, to be applied.</span></span> <span data-ttu-id="94b89-110">Sie werden sequenziell, der niedrigste Index zuerst angewendet.</span><span class="sxs-lookup"><span data-stu-id="94b89-110">They are applied sequentially, lowest index first.</span></span>
<span data-ttu-id="94b89-111">Jeder muss über ein kontrolliertes Funktor verfügen.</span><span class="sxs-lookup"><span data-stu-id="94b89-111">Each must have a Controlled functor</span></span>


### <a name="targets--int"></a><span data-ttu-id="94b89-112">Ziele: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="94b89-112">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="94b89-113">Geschmestete Arrays, die die Ziele des OP beschreiben.</span><span class="sxs-lookup"><span data-stu-id="94b89-113">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="94b89-114">Jedes Array muss eine Liste von Punkten enthalten, in denen die zu verwendenden Indizes beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="94b89-114">Each array should contain a list of ints describing the indices to be used.</span></span>


### <a name="register--t"></a><span data-ttu-id="94b89-115">Register: 't []</span><span class="sxs-lookup"><span data-stu-id="94b89-115">register : 'T[]</span></span>

<span data-ttu-id="94b89-116">Das Qubit-Register, das bearbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="94b89-116">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="94b89-117">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="94b89-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="94b89-118">Typparameter</span><span class="sxs-lookup"><span data-stu-id="94b89-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="94b89-119">GIF</span><span class="sxs-lookup"><span data-stu-id="94b89-119">'T</span></span>



## <a name="see-also"></a><span data-ttu-id="94b89-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="94b89-120">See Also</span></span>

- [<span data-ttu-id="94b89-121">Microsoft. Quantum. Canon. applyoprepeatedlyover</span><span class="sxs-lookup"><span data-stu-id="94b89-121">Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver</span></span>](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)
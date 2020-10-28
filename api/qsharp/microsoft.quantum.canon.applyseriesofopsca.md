---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOpsCA
title: Applyseriesofopsca-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOpsCA
qsharp.summary: Applies a list of ops and their targets sequentially on an array. (Adjoint + Controlled)
ms.openlocfilehash: 2327a693e528cf46f95eae5ee052e9dd9b6ee187
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705007"
---
# <a name="applyseriesofopsca-operation"></a><span data-ttu-id="acedc-102">Applyseriesofopsca-Vorgang</span><span class="sxs-lookup"><span data-stu-id="acedc-102">ApplySeriesOfOpsCA operation</span></span>

<span data-ttu-id="acedc-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="acedc-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="acedc-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="acedc-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="acedc-105">Wendet eine Liste von OPS und deren Zielen sequenziell auf ein Array an.</span><span class="sxs-lookup"><span data-stu-id="acedc-105">Applies a list of ops and their targets sequentially on an array.</span></span> <span data-ttu-id="acedc-106">(Adjoint + gesteuert)</span><span class="sxs-lookup"><span data-stu-id="acedc-106">(Adjoint + Controlled)</span></span>

```qsharp
operation ApplySeriesOfOpsCA<'T> (listOfOps : ('T[] => Unit is Adj + Ctl)[], targets : Int[][], register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="acedc-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="acedc-107">Input</span></span>

### <a name="listofops--t--unit-adj--ctl"></a><span data-ttu-id="acedc-108">listOf: 't [] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL []</span><span class="sxs-lookup"><span data-stu-id="acedc-108">listOfOps : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl[]</span></span>

<span data-ttu-id="acedc-109">Die Liste der OPS, die jeweils ein nicht-Array enthalten, das angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="acedc-109">List of ops, each taking a 'T array, to be applied.</span></span> <span data-ttu-id="acedc-110">Sie werden sequenziell, der niedrigste Index zuerst angewendet.</span><span class="sxs-lookup"><span data-stu-id="acedc-110">They are applied sequentially, lowest index first.</span></span>
<span data-ttu-id="acedc-111">Jede muss sowohl über einen Adjoint-als auch überwachten Funktor verfügen.</span><span class="sxs-lookup"><span data-stu-id="acedc-111">Each must have both an Adjoint and Controlled functor.</span></span>


### <a name="targets--int"></a><span data-ttu-id="acedc-112">Ziele: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="acedc-112">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="acedc-113">Geschmestete Arrays, die die Ziele des OP beschreiben.</span><span class="sxs-lookup"><span data-stu-id="acedc-113">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="acedc-114">Jedes Array muss eine Liste von Punkten enthalten, in denen die zu verwendenden Indizes beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="acedc-114">Each array should contain a list of ints describing the indices to be used.</span></span>


### <a name="register--t"></a><span data-ttu-id="acedc-115">Register: 't []</span><span class="sxs-lookup"><span data-stu-id="acedc-115">register : 'T[]</span></span>

<span data-ttu-id="acedc-116">Das Qubit-Register, das bearbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="acedc-116">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="acedc-117">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="acedc-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="acedc-118">Typparameter</span><span class="sxs-lookup"><span data-stu-id="acedc-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="acedc-119">GIF</span><span class="sxs-lookup"><span data-stu-id="acedc-119">'T</span></span>



## <a name="see-also"></a><span data-ttu-id="acedc-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="acedc-120">See Also</span></span>

- [<span data-ttu-id="acedc-121">Microsoft. Quantum. Canon. applyoprepeatedlyover</span><span class="sxs-lookup"><span data-stu-id="acedc-121">Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver</span></span>](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)
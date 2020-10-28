---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOpsA
title: Applyseriesofopsa-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOpsA
qsharp.summary: Applies a list of ops and their targets sequentially on an array. (Adjoint)
ms.openlocfilehash: e2b928fa4c9446e16d2bf5e7b68a32d4bba3a528
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705018"
---
# <a name="applyseriesofopsa-operation"></a><span data-ttu-id="37bb1-102">Applyseriesofopsa-Vorgang</span><span class="sxs-lookup"><span data-stu-id="37bb1-102">ApplySeriesOfOpsA operation</span></span>

<span data-ttu-id="37bb1-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="37bb1-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="37bb1-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="37bb1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="37bb1-105">Wendet eine Liste von OPS und deren Zielen sequenziell auf ein Array an.</span><span class="sxs-lookup"><span data-stu-id="37bb1-105">Applies a list of ops and their targets sequentially on an array.</span></span> <span data-ttu-id="37bb1-106">(Adjoint)</span><span class="sxs-lookup"><span data-stu-id="37bb1-106">(Adjoint)</span></span>

```qsharp
operation ApplySeriesOfOpsA<'T> (listOfOps : ('T[] => Unit is Adj)[], targets : Int[][], register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="37bb1-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="37bb1-107">Input</span></span>

### <a name="listofops--t--unit-adj"></a><span data-ttu-id="37bb1-108">listOf: 't [] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ []</span><span class="sxs-lookup"><span data-stu-id="37bb1-108">listOfOps : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj[]</span></span>

<span data-ttu-id="37bb1-109">Die Liste der OPS, die jeweils ein nicht-Array enthalten, das angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="37bb1-109">List of ops, each taking a 'T array, to be applied.</span></span> <span data-ttu-id="37bb1-110">Sie werden sequenziell, der niedrigste Index zuerst angewendet.</span><span class="sxs-lookup"><span data-stu-id="37bb1-110">They are applied sequentially, lowest index first.</span></span>
<span data-ttu-id="37bb1-111">Jeder muss über einen Adjoint-Funktions tüktor verfügen.</span><span class="sxs-lookup"><span data-stu-id="37bb1-111">Each must have an adjoint functor</span></span>


### <a name="targets--int"></a><span data-ttu-id="37bb1-112">Ziele: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="37bb1-112">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="37bb1-113">Geschmestete Arrays, die die Ziele des OP beschreiben.</span><span class="sxs-lookup"><span data-stu-id="37bb1-113">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="37bb1-114">Jedes Array muss eine Liste von Punkten enthalten, in denen die zu verwendenden Indizes beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="37bb1-114">Each array should contain a list of ints describing the indices to be used.</span></span>


### <a name="register--t"></a><span data-ttu-id="37bb1-115">Register: 't []</span><span class="sxs-lookup"><span data-stu-id="37bb1-115">register : 'T[]</span></span>

<span data-ttu-id="37bb1-116">Das Qubit-Register, das bearbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="37bb1-116">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="37bb1-117">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="37bb1-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="37bb1-118">Typparameter</span><span class="sxs-lookup"><span data-stu-id="37bb1-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="37bb1-119">GIF</span><span class="sxs-lookup"><span data-stu-id="37bb1-119">'T</span></span>



## <a name="see-also"></a><span data-ttu-id="37bb1-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="37bb1-120">See Also</span></span>

- [<span data-ttu-id="37bb1-121">Microsoft. Quantum. Canon. applyoprepeatedlyover</span><span class="sxs-lookup"><span data-stu-id="37bb1-121">Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver</span></span>](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)
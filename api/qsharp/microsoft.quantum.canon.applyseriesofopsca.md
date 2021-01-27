---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOpsCA
title: Applyseriesofopsca-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOpsCA
qsharp.summary: Applies a list of ops and their targets sequentially on an array. (Adjoint + Controlled)
ms.openlocfilehash: 9a1f6189428b086c38b1d0f289afb18c2cf1be40
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850871"
---
# <a name="applyseriesofopsca-operation"></a><span data-ttu-id="d2ed2-102">Applyseriesofopsca-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d2ed2-102">ApplySeriesOfOpsCA operation</span></span>

<span data-ttu-id="d2ed2-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d2ed2-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d2ed2-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d2ed2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d2ed2-105">Wendet eine Liste von OPS und deren Zielen sequenziell auf ein Array an.</span><span class="sxs-lookup"><span data-stu-id="d2ed2-105">Applies a list of ops and their targets sequentially on an array.</span></span> <span data-ttu-id="d2ed2-106">(Adjoint + gesteuert)</span><span class="sxs-lookup"><span data-stu-id="d2ed2-106">(Adjoint + Controlled)</span></span>

```qsharp
operation ApplySeriesOfOpsCA<'T> (listOfOps : ('T[] => Unit is Adj + Ctl)[], targets : Int[][], register : 'T[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="d2ed2-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d2ed2-107">Input</span></span>

### <a name="listofops--t--unit--is-adj--ctl"></a><span data-ttu-id="d2ed2-108">listOf: 't [] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL []</span><span class="sxs-lookup"><span data-stu-id="d2ed2-108">listOfOps : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl[]</span></span>

<span data-ttu-id="d2ed2-109">Die Liste der OPS, die jeweils ein nicht-Array enthalten, das angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d2ed2-109">List of ops, each taking a 'T array, to be applied.</span></span> <span data-ttu-id="d2ed2-110">Sie werden sequenziell, der niedrigste Index zuerst angewendet.</span><span class="sxs-lookup"><span data-stu-id="d2ed2-110">They are applied sequentially, lowest index first.</span></span>
<span data-ttu-id="d2ed2-111">Jede muss sowohl über einen Adjoint-als auch überwachten Funktor verfügen.</span><span class="sxs-lookup"><span data-stu-id="d2ed2-111">Each must have both an Adjoint and Controlled functor.</span></span>


### <a name="targets--int"></a><span data-ttu-id="d2ed2-112">Ziele: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="d2ed2-112">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="d2ed2-113">Geschmestete Arrays, die die Ziele des OP beschreiben.</span><span class="sxs-lookup"><span data-stu-id="d2ed2-113">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="d2ed2-114">Jedes Array muss eine Liste von Punkten enthalten, in denen die zu verwendenden Indizes beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="d2ed2-114">Each array should contain a list of ints describing the indices to be used.</span></span>


### <a name="register--t"></a><span data-ttu-id="d2ed2-115">Register: 't []</span><span class="sxs-lookup"><span data-stu-id="d2ed2-115">register : 'T[]</span></span>

<span data-ttu-id="d2ed2-116">Das Qubit-Register, das bearbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d2ed2-116">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d2ed2-117">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d2ed2-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="d2ed2-118">Typparameter</span><span class="sxs-lookup"><span data-stu-id="d2ed2-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d2ed2-119">GIF</span><span class="sxs-lookup"><span data-stu-id="d2ed2-119">'T</span></span>



## <a name="example"></a><span data-ttu-id="d2ed2-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d2ed2-120">Example</span></span>

<span data-ttu-id="d2ed2-121">Folgendes gilt für Exp ([Paulix, pauliy], 0,5) für Qubits 0, 1//dann X bis Qubit 2 Let OPS = [Exp ([Paulix, pauliy], 0,5, _), applyjefirstqubitca (X, _)]; Let-Indizes = [[0, 1], [2]]; Applyseriesofopsca (OPS, Indizes, qubitarray);</span><span class="sxs-lookup"><span data-stu-id="d2ed2-121">// The following applies Exp([PauliX, PauliY], 0.5) to qubits 0, 1 // then X to qubit 2 let ops = [Exp([PauliX, PauliY], 0.5, _), ApplyToFirstQubitCA(X, _)]; let indices = [[0, 1], [2]]; ApplySeriesOfOpsCA(ops, indices, qubitArray);</span></span>

## <a name="see-also"></a><span data-ttu-id="d2ed2-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d2ed2-122">See Also</span></span>

- [<span data-ttu-id="d2ed2-123">Microsoft. Quantum. Canon. applyoprepeatedlyover</span><span class="sxs-lookup"><span data-stu-id="d2ed2-123">Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver</span></span>](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)
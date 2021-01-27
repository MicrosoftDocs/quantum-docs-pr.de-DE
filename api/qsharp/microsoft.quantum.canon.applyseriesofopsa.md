---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOpsA
title: Applyseriesofopsa-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOpsA
qsharp.summary: Applies a list of ops and their targets sequentially on an array. (Adjoint)
ms.openlocfilehash: 052cb52d4ee6500e60043ab7f808497058924afe
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844662"
---
# <a name="applyseriesofopsa-operation"></a><span data-ttu-id="b72df-102">Applyseriesofopsa-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b72df-102">ApplySeriesOfOpsA operation</span></span>

<span data-ttu-id="b72df-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="b72df-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="b72df-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b72df-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b72df-105">Wendet eine Liste von OPS und deren Zielen sequenziell auf ein Array an.</span><span class="sxs-lookup"><span data-stu-id="b72df-105">Applies a list of ops and their targets sequentially on an array.</span></span> <span data-ttu-id="b72df-106">(Adjoint)</span><span class="sxs-lookup"><span data-stu-id="b72df-106">(Adjoint)</span></span>

```qsharp
operation ApplySeriesOfOpsA<'T> (listOfOps : ('T[] => Unit is Adj)[], targets : Int[][], register : 'T[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="b72df-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b72df-107">Input</span></span>

### <a name="listofops--t--unit--is-adj"></a><span data-ttu-id="b72df-108">listOf: 't [] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ []</span><span class="sxs-lookup"><span data-stu-id="b72df-108">listOfOps : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj[]</span></span>

<span data-ttu-id="b72df-109">Die Liste der OPS, die jeweils ein nicht-Array enthalten, das angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b72df-109">List of ops, each taking a 'T array, to be applied.</span></span> <span data-ttu-id="b72df-110">Sie werden sequenziell, der niedrigste Index zuerst angewendet.</span><span class="sxs-lookup"><span data-stu-id="b72df-110">They are applied sequentially, lowest index first.</span></span>
<span data-ttu-id="b72df-111">Jeder muss über einen Adjoint-Funktions tüktor verfügen.</span><span class="sxs-lookup"><span data-stu-id="b72df-111">Each must have an adjoint functor</span></span>


### <a name="targets--int"></a><span data-ttu-id="b72df-112">Ziele: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="b72df-112">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="b72df-113">Geschmestete Arrays, die die Ziele des OP beschreiben.</span><span class="sxs-lookup"><span data-stu-id="b72df-113">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="b72df-114">Jedes Array muss eine Liste von Punkten enthalten, in denen die zu verwendenden Indizes beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="b72df-114">Each array should contain a list of ints describing the indices to be used.</span></span>


### <a name="register--t"></a><span data-ttu-id="b72df-115">Register: 't []</span><span class="sxs-lookup"><span data-stu-id="b72df-115">register : 'T[]</span></span>

<span data-ttu-id="b72df-116">Das Qubit-Register, das bearbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b72df-116">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b72df-117">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b72df-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="b72df-118">Typparameter</span><span class="sxs-lookup"><span data-stu-id="b72df-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="b72df-119">GIF</span><span class="sxs-lookup"><span data-stu-id="b72df-119">'T</span></span>



## <a name="example"></a><span data-ttu-id="b72df-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b72df-120">Example</span></span>

<span data-ttu-id="b72df-121">Folgendes gilt für Exp ([Paulix, pauliy], 0,5) für Qubits 0, 1//dann X bis Qubit 2 Let OPS = [Exp ([Paulix, pauliy], 0,5, _), applyjefirstqubita (X, _)]; Let-Indizes = [[0, 1], [2]]; Applyseriesofopsa (OPS, Indizes, qubitarray);</span><span class="sxs-lookup"><span data-stu-id="b72df-121">// The following applies Exp([PauliX, PauliY], 0.5) to qubits 0, 1 // then X to qubit 2 let ops = [Exp([PauliX, PauliY], 0.5, _), ApplyToFirstQubitA(X, _)]; let indices = [[0, 1], [2]]; ApplySeriesOfOpsA(ops, indices, qubitArray);</span></span>

## <a name="see-also"></a><span data-ttu-id="b72df-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b72df-122">See Also</span></span>

- [<span data-ttu-id="b72df-123">Microsoft. Quantum. Canon. applyoprepeatedlyover</span><span class="sxs-lookup"><span data-stu-id="b72df-123">Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver</span></span>](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)
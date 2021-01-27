---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOpsC
title: Applyseriesofopsc-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOpsC
qsharp.summary: Applies a list of ops and their targets sequentially on an array. (Controlled)
ms.openlocfilehash: 308256833dc607f685e3a5f2278e374cf3b6ce22
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844645"
---
# <a name="applyseriesofopsc-operation"></a><span data-ttu-id="35545-102">Applyseriesofopsc-Vorgang</span><span class="sxs-lookup"><span data-stu-id="35545-102">ApplySeriesOfOpsC operation</span></span>

<span data-ttu-id="35545-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="35545-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="35545-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="35545-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="35545-105">Wendet eine Liste von OPS und deren Zielen sequenziell auf ein Array an.</span><span class="sxs-lookup"><span data-stu-id="35545-105">Applies a list of ops and their targets sequentially on an array.</span></span> <span data-ttu-id="35545-106">Klimatisiert</span><span class="sxs-lookup"><span data-stu-id="35545-106">(Controlled)</span></span>

```qsharp
operation ApplySeriesOfOpsC<'T> (listOfOps : ('T[] => Unit is Ctl)[], targets : Int[][], register : 'T[]) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="35545-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="35545-107">Input</span></span>

### <a name="listofops--t--unit--is-ctl"></a><span data-ttu-id="35545-108">listOf: 't [] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL []</span><span class="sxs-lookup"><span data-stu-id="35545-108">listOfOps : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl[]</span></span>

<span data-ttu-id="35545-109">Die Liste der OPS, die jeweils ein nicht-Array enthalten, das angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="35545-109">List of ops, each taking a 'T array, to be applied.</span></span> <span data-ttu-id="35545-110">Sie werden sequenziell, der niedrigste Index zuerst angewendet.</span><span class="sxs-lookup"><span data-stu-id="35545-110">They are applied sequentially, lowest index first.</span></span>
<span data-ttu-id="35545-111">Jeder muss über ein kontrolliertes Funktor verfügen.</span><span class="sxs-lookup"><span data-stu-id="35545-111">Each must have a Controlled functor</span></span>


### <a name="targets--int"></a><span data-ttu-id="35545-112">Ziele: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="35545-112">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="35545-113">Geschmestete Arrays, die die Ziele des OP beschreiben.</span><span class="sxs-lookup"><span data-stu-id="35545-113">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="35545-114">Jedes Array muss eine Liste von Punkten enthalten, in denen die zu verwendenden Indizes beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="35545-114">Each array should contain a list of ints describing the indices to be used.</span></span>


### <a name="register--t"></a><span data-ttu-id="35545-115">Register: 't []</span><span class="sxs-lookup"><span data-stu-id="35545-115">register : 'T[]</span></span>

<span data-ttu-id="35545-116">Das Qubit-Register, das bearbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="35545-116">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="35545-117">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="35545-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="35545-118">Typparameter</span><span class="sxs-lookup"><span data-stu-id="35545-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="35545-119">GIF</span><span class="sxs-lookup"><span data-stu-id="35545-119">'T</span></span>



## <a name="example"></a><span data-ttu-id="35545-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="35545-120">Example</span></span>

<span data-ttu-id="35545-121">Folgendes gilt für Exp ([Paulix, pauliy], 0,5) für Qubits 0, 1//dann X bis Qubit 2 Let OPS = [Exp ([Paulix, pauliy], 0,5, _), applyjefirstqubitc (X, _)]; Let-Indizes = [[0, 1], [2]]; Applyseriesofopsc (OPS, Indizes, qubitarray);</span><span class="sxs-lookup"><span data-stu-id="35545-121">// The following applies Exp([PauliX, PauliY], 0.5) to qubits 0, 1 // then X to qubit 2 let ops = [Exp([PauliX, PauliY], 0.5, _), ApplyToFirstQubitC(X, _)]; let indices = [[0, 1], [2]]; ApplySeriesOfOpsC(ops, indices, qubitArray);</span></span>

## <a name="see-also"></a><span data-ttu-id="35545-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="35545-122">See Also</span></span>

- [<span data-ttu-id="35545-123">Microsoft. Quantum. Canon. applyoprepeatedlyover</span><span class="sxs-lookup"><span data-stu-id="35545-123">Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver</span></span>](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)
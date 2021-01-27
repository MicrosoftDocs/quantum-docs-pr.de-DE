---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOps
title: Applyseriesofops-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOps
qsharp.summary: Applies a list of ops and their targets sequentially on an array.
ms.openlocfilehash: b086b01b0be86bd25a6d6cdef26bfbb53e484cb2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841496"
---
# <a name="applyseriesofops-operation"></a><span data-ttu-id="e3e76-102">Applyseriesofops-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e3e76-102">ApplySeriesOfOps operation</span></span>

<span data-ttu-id="e3e76-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e3e76-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e3e76-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e3e76-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e3e76-105">Wendet eine Liste von OPS und deren Zielen sequenziell auf ein Array an.</span><span class="sxs-lookup"><span data-stu-id="e3e76-105">Applies a list of ops and their targets sequentially on an array.</span></span>

```qsharp
operation ApplySeriesOfOps<'T> (listOfOps : ('T[] => Unit)[], targets : Int[][], register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="e3e76-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e3e76-106">Input</span></span>

### <a name="listofops--t--unit-"></a><span data-ttu-id="e3e76-107">listOf: 't [] => [Unit](xref:microsoft.quantum.lang-ref.unit) []</span><span class="sxs-lookup"><span data-stu-id="e3e76-107">listOfOps : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit) []</span></span>

<span data-ttu-id="e3e76-108">Die Liste der OPS, die jeweils ein nicht-Array enthalten, das angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e3e76-108">List of ops, each taking a 'T array, to be applied.</span></span> <span data-ttu-id="e3e76-109">Sie werden sequenziell, der niedrigste Index zuerst angewendet.</span><span class="sxs-lookup"><span data-stu-id="e3e76-109">They are applied sequentially, lowest index first.</span></span>


### <a name="targets--int"></a><span data-ttu-id="e3e76-110">Ziele: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="e3e76-110">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="e3e76-111">Geschmestete Arrays, die die Ziele des OP beschreiben.</span><span class="sxs-lookup"><span data-stu-id="e3e76-111">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="e3e76-112">Jedes Array muss eine Liste von Punkten enthalten, in denen die zu verwendenden Indizes beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="e3e76-112">Each array should contain a list of ints describing the indices to be used.</span></span>


### <a name="register--t"></a><span data-ttu-id="e3e76-113">Register: 't []</span><span class="sxs-lookup"><span data-stu-id="e3e76-113">register : 'T[]</span></span>

<span data-ttu-id="e3e76-114">Das Qubit-Register, das bearbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e3e76-114">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e3e76-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e3e76-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="e3e76-116">Typparameter</span><span class="sxs-lookup"><span data-stu-id="e3e76-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e3e76-117">GIF</span><span class="sxs-lookup"><span data-stu-id="e3e76-117">'T</span></span>



## <a name="example"></a><span data-ttu-id="e3e76-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e3e76-118">Example</span></span>

<span data-ttu-id="e3e76-119">Folgendes gilt für Exp ([Paulix, pauliy], 0,5) für Qubits 0, 1//dann X bis Qubit 2 Let OPS = [Exp ([Paulix, pauliy], 0,5, _), applyjefirstqubit (X, _)]; Let-Indizes = [[0, 1], [2]]; Applyseriesofops (OPS, Indizes, qubitarray);</span><span class="sxs-lookup"><span data-stu-id="e3e76-119">// The following applies Exp([PauliX, PauliY], 0.5) to qubits 0, 1 // then X to qubit 2 let ops = [Exp([PauliX, PauliY], 0.5, _), ApplyToFirstQubit(X, _)]; let indices = [[0, 1], [2]]; ApplySeriesOfOps(ops, indices, qubitArray);</span></span>

## <a name="see-also"></a><span data-ttu-id="e3e76-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e3e76-120">See Also</span></span>

- [<span data-ttu-id="e3e76-121">Microsoft. Quantum. Canon. applyoprepeatedlyover</span><span class="sxs-lookup"><span data-stu-id="e3e76-121">Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver</span></span>](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)
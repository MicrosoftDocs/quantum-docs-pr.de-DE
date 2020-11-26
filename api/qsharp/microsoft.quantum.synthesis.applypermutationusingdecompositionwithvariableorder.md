---
uid: Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecompositionWithVariableOrder
title: Applypermutationusingdecompositionwithvariableorder-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyPermutationUsingDecompositionWithVariableOrder
qsharp.summary: Permutes the amplitudes in a quantum state given a permutation using decomposition-based synthesis.
ms.openlocfilehash: a5ca9b366f7ff477070e21fea047ff04b425439c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203432"
---
# <a name="applypermutationusingdecompositionwithvariableorder-operation"></a><span data-ttu-id="d75c7-102">Applypermutationusingdecompositionwithvariableorder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d75c7-102">ApplyPermutationUsingDecompositionWithVariableOrder operation</span></span>

<span data-ttu-id="d75c7-103">Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="d75c7-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="d75c7-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d75c7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d75c7-105">Pertrauert die Verstärkung in einem Quantum-Zustand, wenn eine permutations mithilfe der Zerlegungs basierten Synthese verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d75c7-105">Permutes the amplitudes in a quantum state given a permutation using decomposition-based synthesis.</span></span>

```qsharp
operation ApplyPermutationUsingDecompositionWithVariableOrder (perm : Int[], variableOrder : Int[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="d75c7-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d75c7-106">Description</span></span>

<span data-ttu-id="d75c7-107">Bei diesem Vorgang handelt es sich um eine allgemeinere Version von @"microsoft.quantum.synthesis.applypermutationusingdecomposition" , in der die Reihenfolge der Variablen angegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="d75c7-107">This operation is a more general version of @"microsoft.quantum.synthesis.applypermutationusingdecomposition" in which the variable order can be specified.</span></span> <span data-ttu-id="d75c7-108">Eine andere Variablen Reihenfolge ändert die Zerlegungs Sequenz und die Wahrheitstabellen, die für die kontrollierten Gates verwendet werden @"microsoft.quantum.intrinsic.x" .</span><span class="sxs-lookup"><span data-stu-id="d75c7-108">A different variable order changes the decomposition sequence and the truth tables used for the controlled @"microsoft.quantum.intrinsic.x" gates.</span></span>  <span data-ttu-id="d75c7-109">Wenn Sie die Reihenfolge der Variablen ändern, wird daher die Gesamtzahl der Gates geändert, die zur Umsetzung der Permutation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d75c7-109">Therefore, changing the variable order changes the number of overall gates used to realize the permutation.</span></span>

## <a name="input"></a><span data-ttu-id="d75c7-110">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d75c7-110">Input</span></span>

### <a name="perm--int"></a><span data-ttu-id="d75c7-111">Perm: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="d75c7-111">perm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="d75c7-112">Eine permutations von $2 ^ n $ Elementen, beginnend bei 0.</span><span class="sxs-lookup"><span data-stu-id="d75c7-112">A permutation of $2^n$ elements starting from 0.</span></span>


### <a name="variableorder--int"></a><span data-ttu-id="d75c7-113">variableorder: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="d75c7-113">variableOrder : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="d75c7-114">Eine permutations von $n $-Elementen, beginnend bei 0.</span><span class="sxs-lookup"><span data-stu-id="d75c7-114">A permutation of $n$ elements starting from 0.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="d75c7-115">Qubits: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="d75c7-115">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="d75c7-116">Eine Liste von $n $ Qubits, auf die die permutations angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="d75c7-116">A list of $n$ qubits to which the permutation is applied to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d75c7-117">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d75c7-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="d75c7-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d75c7-118">See Also</span></span>

- [<span data-ttu-id="d75c7-119">Microsoft. Quantum. Synthese. applypermutationusingzerlegung</span><span class="sxs-lookup"><span data-stu-id="d75c7-119">Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition</span></span>](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition)
- [<span data-ttu-id="d75c7-120">Microsoft. Quantum. Synthese. applypermutationusingtransformation</span><span class="sxs-lookup"><span data-stu-id="d75c7-120">Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation</span></span>](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation)
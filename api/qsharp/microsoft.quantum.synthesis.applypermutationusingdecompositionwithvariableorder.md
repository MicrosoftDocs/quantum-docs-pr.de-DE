---
uid: Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecompositionWithVariableOrder
title: Applypermutationusingdecompositionwithvariableorder-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyPermutationUsingDecompositionWithVariableOrder
qsharp.summary: Permutes the amplitudes in a quantum state given a permutation using decomposition-based synthesis.
ms.openlocfilehash: 1edbc0a2948fdf3ae67f14b3c552676feaa7f498
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725299"
---
# <a name="applypermutationusingdecompositionwithvariableorder-operation"></a><span data-ttu-id="1924a-102">Applypermutationusingdecompositionwithvariableorder-Vorgang</span><span class="sxs-lookup"><span data-stu-id="1924a-102">ApplyPermutationUsingDecompositionWithVariableOrder operation</span></span>

<span data-ttu-id="1924a-103">Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="1924a-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="1924a-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1924a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="1924a-105">Pertrauert die Verstärkung in einem Quantum-Zustand, wenn eine permutations mithilfe der Zerlegungs basierten Synthese verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1924a-105">Permutes the amplitudes in a quantum state given a permutation using decomposition-based synthesis.</span></span>

```qsharp
operation ApplyPermutationUsingDecompositionWithVariableOrder (perm : Int[], variableOrder : Int[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="1924a-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1924a-106">Description</span></span>

<span data-ttu-id="1924a-107">Bei diesem Vorgang handelt es sich um eine allgemeinere Version von @"microsoft.quantum.synthesis.applypermutationusingdecomposition" , in der die Reihenfolge der Variablen angegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="1924a-107">This operation is a more general version of @"microsoft.quantum.synthesis.applypermutationusingdecomposition" in which the variable order can be specified.</span></span> <span data-ttu-id="1924a-108">Eine andere Variablen Reihenfolge ändert die Zerlegungs Sequenz und die Wahrheitstabellen, die für die kontrollierten Gates verwendet werden @"microsoft.quantum.intrinsic.x" .</span><span class="sxs-lookup"><span data-stu-id="1924a-108">A different variable order changes the decomposition sequence and the truth tables used for the controlled @"microsoft.quantum.intrinsic.x" gates.</span></span>  <span data-ttu-id="1924a-109">Wenn Sie die Reihenfolge der Variablen ändern, wird daher die Gesamtzahl der Gates geändert, die zur Umsetzung der Permutation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1924a-109">Therefore, changing the variable order changes the number of overall gates used to realize the permutation.</span></span>

## <a name="input"></a><span data-ttu-id="1924a-110">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1924a-110">Input</span></span>

### <a name="perm--int"></a><span data-ttu-id="1924a-111">Perm: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="1924a-111">perm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="1924a-112">Eine permutations von $2 ^ n $ Elementen, beginnend bei 0.</span><span class="sxs-lookup"><span data-stu-id="1924a-112">A permutation of $2^n$ elements starting from 0.</span></span>


### <a name="variableorder--int"></a><span data-ttu-id="1924a-113">variableorder: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="1924a-113">variableOrder : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="1924a-114">Eine permutations von $n $-Elementen, beginnend bei 0.</span><span class="sxs-lookup"><span data-stu-id="1924a-114">A permutation of $n$ elements starting from 0.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="1924a-115">Qubits: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="1924a-115">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="1924a-116">Eine Liste von $n $ Qubits, auf die die permutations angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="1924a-116">A list of $n$ qubits to which the permutation is applied to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1924a-117">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1924a-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="1924a-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1924a-118">See Also</span></span>

- [<span data-ttu-id="1924a-119">Microsoft. Quantum. Synthese. applypermutationusingzerlegung</span><span class="sxs-lookup"><span data-stu-id="1924a-119">Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition</span></span>](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition)
- [<span data-ttu-id="1924a-120">Microsoft. Quantum. Synthese. applypermutationusingtransformation</span><span class="sxs-lookup"><span data-stu-id="1924a-120">Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation</span></span>](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation)
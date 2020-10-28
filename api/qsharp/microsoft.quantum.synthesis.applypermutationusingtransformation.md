---
uid: Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation
title: Applypermutationusingtransformation-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyPermutationUsingTransformation
qsharp.summary: Permutes the amplitudes in a quantum state given a permutation using transformation-based synthesis.
ms.openlocfilehash: b7196c592690a00da49b17f52b30536ba97b6035
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725286"
---
# <a name="applypermutationusingtransformation-operation"></a><span data-ttu-id="33ecf-102">Applypermutationusingtransformation-Vorgang</span><span class="sxs-lookup"><span data-stu-id="33ecf-102">ApplyPermutationUsingTransformation operation</span></span>

<span data-ttu-id="33ecf-103">Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="33ecf-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="33ecf-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="33ecf-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="33ecf-105">Pertrauert die Verstärkung in einem Quantum-Zustand, wenn eine permutations mithilfe der Transformations basierten Synthese verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="33ecf-105">Permutes the amplitudes in a quantum state given a permutation using transformation-based synthesis.</span></span>

```qsharp
operation ApplyPermutationUsingTransformation (perm : Int[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="33ecf-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="33ecf-106">Description</span></span>

<span data-ttu-id="33ecf-107">Diese Prozedur implementiert den unidirektionalen Transformations basierten Synthese Ansatz.</span><span class="sxs-lookup"><span data-stu-id="33ecf-107">This procedure implements the unidirectional transformation based synthesis approach.</span></span>  <span data-ttu-id="33ecf-108">Input ist eine permutations $ \pi $ over $2 ^ n $ Elements $ \{ 0, \dots, 2 ^ n-1 \} $, was eine $n $-Variable umkehrbare boolesche Funktion darstellt.</span><span class="sxs-lookup"><span data-stu-id="33ecf-108">Input is a permutation $\pi$ over $2^n$ elements $\{0, \dots, 2^n-1\}$, which represents an $n$-variable reversible Boolean function.</span></span>
<span data-ttu-id="33ecf-109">Der Algorithmus führt iterativ die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="33ecf-109">The algorithm performs iteratively the following steps:</span></span>

1. <span data-ttu-id="33ecf-110">Suchen Sie den kleinsten $x $, sodass $x \nE \pi (x) = y $.</span><span class="sxs-lookup"><span data-stu-id="33ecf-110">Find smallest $x$ such that $x \ne \pi(x) = y$.</span></span>
2. <span data-ttu-id="33ecf-111">Suchen von multigesteuerten Toffoli-Vorgängen, die auf die Ausgaben angewendet werden, machen $ \pi (x) = x $ und ändern $ \pi (x ') $ nicht für alle $x ' < x $</span><span class="sxs-lookup"><span data-stu-id="33ecf-111">Find multiple-controlled Toffoli operations, which applied to the outputs make $\pi(x) = x$ and do not change $\pi(x')$ for all $x' < x$</span></span>

## <a name="input"></a><span data-ttu-id="33ecf-112">Eingabe</span><span class="sxs-lookup"><span data-stu-id="33ecf-112">Input</span></span>

### <a name="perm--int"></a><span data-ttu-id="33ecf-113">Perm: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="33ecf-113">perm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="33ecf-114">Eine permutations von $2 ^ n $ Elementen, beginnend bei 0.</span><span class="sxs-lookup"><span data-stu-id="33ecf-114">A permutation of $2^n$ elements starting from 0.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="33ecf-115">Qubits: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="33ecf-115">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="33ecf-116">Eine Liste von $n $ Qubits, auf die die permutations angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="33ecf-116">A list of $n$ qubits to which the permutation is applied to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="33ecf-117">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="33ecf-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="33ecf-118">Referenzen</span><span class="sxs-lookup"><span data-stu-id="33ecf-118">References</span></span>

- [<span data-ttu-id="33ecf-119">*D. Michael Miller* , *Dmitri Maslov* , *Gerhard W. Dueck* , proc. DAC 2003, IEEE, pp. 318-323, 2003</span><span class="sxs-lookup"><span data-stu-id="33ecf-119">*D. Michael Miller* , *Dmitri Maslov* , *Gerhard W. Dueck* , Proc. DAC 2003, IEEE, pp. 318-323, 2003</span></span>](https://doi.org/10.1145/775832.775915)
- [<span data-ttu-id="33ecf-120">*Mathias soeken* , *Gerhard W. Dueck* , *D. Michael Miller* , proc. RC 2016, Springer, pp. 307-321, 2016</span><span class="sxs-lookup"><span data-stu-id="33ecf-120">*Mathias Soeken* , *Gerhard W. Dueck* , *D. Michael Miller* , Proc. RC 2016, Springer, pp. 307-321, 2016</span></span>](https://doi.org/10.1007/978-3-319-40578-0_22)

## <a name="see-also"></a><span data-ttu-id="33ecf-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="33ecf-121">See Also</span></span>

- [<span data-ttu-id="33ecf-122">Microsoft. Quantum. Synthese. applypermutationusingzerlegung</span><span class="sxs-lookup"><span data-stu-id="33ecf-122">Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition</span></span>](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition)
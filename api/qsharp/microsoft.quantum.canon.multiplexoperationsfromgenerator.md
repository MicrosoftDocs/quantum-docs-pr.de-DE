---
uid: Microsoft.Quantum.Canon.MultiplexOperationsFromGenerator
title: Multiplexoperationsfromgenerator-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexOperationsFromGenerator
qsharp.summary: >-
  Applies a multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by n-qubit number state $\ket{j}$.

  $U = \sum^{N-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.
ms.openlocfilehash: 2fde0bf391568f39128e6dca4b535aa6b78407c2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703967"
---
# <a name="multiplexoperationsfromgenerator-operation"></a><span data-ttu-id="98f84-102">Multiplexoperationsfromgenerator-Vorgang</span><span class="sxs-lookup"><span data-stu-id="98f84-102">MultiplexOperationsFromGenerator operation</span></span>

<span data-ttu-id="98f84-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="98f84-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="98f84-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="98f84-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="98f84-105">Wendet einen mehrfach gesteuerten einheitlichen Vorgang $U $ an, der eine einheitliche $V _J $ anwendet, wenn dies durch den n-Qubit-Zahlen Status $ \ket{j} $ gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="98f84-105">Applies a multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by n-qubit number state $\ket{j}$.</span></span>

<span data-ttu-id="98f84-106">$U = \sum ^ {N-1} _ {j = 0} \ket{j}\bra{j}\otimes V_j $.</span><span class="sxs-lookup"><span data-stu-id="98f84-106">$U = \sum^{N-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.</span></span>

```qsharp
operation MultiplexOperationsFromGenerator<'T> (unitaryGenerator : (Int, (Int -> ('T => Unit is Adj + Ctl))), index : Microsoft.Quantum.Arithmetic.LittleEndian, target : 'T) : Unit
```


## <a name="input"></a><span data-ttu-id="98f84-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="98f84-107">Input</span></span>

### <a name="unitarygenerator--intint---t--unit-adj--ctl"></a><span data-ttu-id="98f84-108">unitarygenerator: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int) -> 't => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL)</span><span class="sxs-lookup"><span data-stu-id="98f84-108">unitaryGenerator : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int) -> 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl)</span></span>

<span data-ttu-id="98f84-109">Ein Tupel, bei dem das erste Element `Int` die Anzahl von uniflüssen $N $ und das zweite Element `(Int -> ('T => () is Adj + Ctl))` eine Funktion ist, die eine ganze Zahl $j $ in $ [0, N-1] $ annimmt und den einheitlichen Vorgang $V _J $ ausgibt.</span><span class="sxs-lookup"><span data-stu-id="98f84-109">A tuple where the first element `Int` is the number of unitaries $N$, and the second element `(Int -> ('T => () is Adj + Ctl))` is a function that takes an integer $j$ in $[0,N-1]$ and outputs the unitary operation $V_j$.</span></span>


### <a name="index--littleendian"></a><span data-ttu-id="98f84-110">Index: [littleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="98f84-110">index : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="98f84-111">$n $-Qubit-Steuerelement Register, das die Anzahl der Zustände $ \ket{j} $ im Little-Endian-Format codiert.</span><span class="sxs-lookup"><span data-stu-id="98f84-111">$n$-qubit control register that encodes number states $\ket{j}$ in little-endian format.</span></span>


### <a name="target--t"></a><span data-ttu-id="98f84-112">Ziel: 't</span><span class="sxs-lookup"><span data-stu-id="98f84-112">target : 'T</span></span>

<span data-ttu-id="98f84-113">Generisches Qubit-Register, für das $V _J $ agiert.</span><span class="sxs-lookup"><span data-stu-id="98f84-113">Generic qubit register that $V_j$ acts on.</span></span>



## <a name="output--unit"></a><span data-ttu-id="98f84-114">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="98f84-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="98f84-115">Typparameter</span><span class="sxs-lookup"><span data-stu-id="98f84-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="98f84-116">GIF</span><span class="sxs-lookup"><span data-stu-id="98f84-116">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="98f84-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="98f84-117">Remarks</span></span>

<span data-ttu-id="98f84-118">`coefficients` wird mit Identitäts Elementen aufgefüllt, wenn weniger als $2 ^ n $ angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="98f84-118">`coefficients` will be padded with identity elements if fewer than $2^n$ are specified.</span></span> <span data-ttu-id="98f84-119">Diese Implementierung verwendet $n-$1-hilfssbits.</span><span class="sxs-lookup"><span data-stu-id="98f84-119">This implementation uses $n-1$ auxiliary qubits.</span></span>

## <a name="references"></a><span data-ttu-id="98f84-120">Referenzen</span><span class="sxs-lookup"><span data-stu-id="98f84-120">References</span></span>

- [<span data-ttu-id="98f84-121">*Andrew M. Childs, Dmitri Maslov, yunabong Nam, Neil J. Ross, Yuan su* , arXiv: 1711.10980</span><span class="sxs-lookup"><span data-stu-id="98f84-121"> *Andrew M. Childs, Dmitri Maslov, Yunseong Nam, Neil J. Ross, Yuan Su* , arXiv:1711.10980</span></span>](https://arxiv.org/abs/1711.10980)
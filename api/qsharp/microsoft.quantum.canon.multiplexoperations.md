---
uid: Microsoft.Quantum.Canon.MultiplexOperations
title: Multiplexoperations-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexOperations
qsharp.summary: >-
  Applies an array of operations controlled by an array of number states.

  That is, applies Multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by $n$-qubit number state $\ket{j}$.

  $U = \sum^{2^n-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.
ms.openlocfilehash: ad66b39fcfacbe5231ec3b9ba96989d6d5d449c1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96206101"
---
# <a name="multiplexoperations-operation"></a><span data-ttu-id="b4398-102">Multiplexoperations-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b4398-102">MultiplexOperations operation</span></span>

<span data-ttu-id="b4398-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="b4398-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="b4398-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b4398-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b4398-105">Wendet ein Array von Vorgängen an, die von einem Array von Zahlen Zuständen gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="b4398-105">Applies an array of operations controlled by an array of number states.</span></span>

<span data-ttu-id="b4398-106">Das heißt, dass der mehrfach gesteuerte einheitliche Vorgang $U $ angewendet wird, der eine einheitliche $V _J $ anwendet, wenn dies durch $n $-Qubit-Zahlen Status $ \ket{j} $ gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="b4398-106">That is, applies Multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by $n$-qubit number state $\ket{j}$.</span></span>

<span data-ttu-id="b4398-107">$U = \sum ^ {2 ^ n-1} _ {j = 0} \ket{j}\bra{j}\otimes V_j $.</span><span class="sxs-lookup"><span data-stu-id="b4398-107">$U = \sum^{2^n-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.</span></span>

```qsharp
operation MultiplexOperations<'T> (unitaries : ('T => Unit is Adj + Ctl)[], index : Microsoft.Quantum.Arithmetic.LittleEndian, target : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="b4398-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b4398-108">Input</span></span>

### <a name="unitaries--t--unit--is-adj--ctl"></a><span data-ttu-id="b4398-109">Uni-Zuflüsse: 't => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL []</span><span class="sxs-lookup"><span data-stu-id="b4398-109">unitaries : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl[]</span></span>

<span data-ttu-id="b4398-110">Array von bis zu $2 ^ n $ einheitlichen Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="b4398-110">Array of up to $2^n$ unitary operations.</span></span> <span data-ttu-id="b4398-111">Der $j $ Th-Vorgang wird durch den Zahlen Status $ \ket{j} $ codiert, der im Little-Endian-Format codiert ist.</span><span class="sxs-lookup"><span data-stu-id="b4398-111">The $j$th operation is indexed by the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="index--littleendian"></a><span data-ttu-id="b4398-112">Index: [littleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="b4398-112">index : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="b4398-113">$n $-Qubit-Steuerelement Register, das die Anzahl der Zustände $ \ket{j} $ im Little-Endian-Format codiert.</span><span class="sxs-lookup"><span data-stu-id="b4398-113">$n$-qubit control register that encodes number states $\ket{j}$ in little-endian format.</span></span>


### <a name="target--t"></a><span data-ttu-id="b4398-114">Ziel: 't</span><span class="sxs-lookup"><span data-stu-id="b4398-114">target : 'T</span></span>

<span data-ttu-id="b4398-115">Generisches Qubit-Register, für das $V _J $ agiert.</span><span class="sxs-lookup"><span data-stu-id="b4398-115">Generic qubit register that $V_j$ acts on.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b4398-116">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b4398-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="b4398-117">Typparameter</span><span class="sxs-lookup"><span data-stu-id="b4398-117">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="b4398-118">GIF</span><span class="sxs-lookup"><span data-stu-id="b4398-118">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="b4398-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b4398-119">Remarks</span></span>

<span data-ttu-id="b4398-120">`coefficients` wird mit Identitäts Elementen aufgefüllt, wenn weniger als $2 ^ n $ angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b4398-120">`coefficients` will be padded with identity elements if fewer than $2^n$ are specified.</span></span> <span data-ttu-id="b4398-121">Diese Implementierung verwendet $n-$1-hilfssbits.</span><span class="sxs-lookup"><span data-stu-id="b4398-121">This implementation uses $n - 1$ auxiliary qubits.</span></span>

## <a name="references"></a><span data-ttu-id="b4398-122">Referenzen</span><span class="sxs-lookup"><span data-stu-id="b4398-122">References</span></span>

- <span data-ttu-id="b4398-123">Zur ersten Quantum-Simulation mit Quantum Beschleunigung Andrew M. Childs, Dmitri Maslov, yunabong Nam, Neil J. Ross, Yuan su https://arxiv.org/abs/1711.10980</span><span class="sxs-lookup"><span data-stu-id="b4398-123">Toward the first quantum simulation with quantum speedup Andrew M. Childs, Dmitri Maslov, Yunseong Nam, Neil J. Ross, Yuan Su https://arxiv.org/abs/1711.10980</span></span>
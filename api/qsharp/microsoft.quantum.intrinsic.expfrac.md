---
uid: Microsoft.Quantum.Intrinsic.ExpFrac
title: Expfrac-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: ExpFrac
qsharp.summary: >-
  Applies the exponential of a multi-qubit Pauli operator with an argument given by a dyadic fraction.

  \begin{align} e^{i \pi k [P_0 \otimes P_1 \cdots P_{N-1}] / 2^n}, \end{align} where $P_i$ is the $i$th element of `paulis`, and where $N = $`Length(paulis)`.
ms.openlocfilehash: 8ccea068dd61aaf8c1ba384969adef5644e8401e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198994"
---
# <a name="expfrac-operation"></a><span data-ttu-id="baae3-102">Expfrac-Vorgang</span><span class="sxs-lookup"><span data-stu-id="baae3-102">ExpFrac operation</span></span>

<span data-ttu-id="baae3-103">Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="baae3-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="baae3-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="baae3-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="baae3-105">Wendet den Exponentialwert eines multiqubit-Pauli-Operators mit einem Argument an, das von einem dyadic-Bruchteil angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="baae3-105">Applies the exponential of a multi-qubit Pauli operator with an argument given by a dyadic fraction.</span></span>

<span data-ttu-id="baae3-106">\begin{align} e ^ {i \pi k [P_0 \otimes P_1 \cdots P_ {N-1}]/2 ^ N}, \end{align}, wobei $P _I $ das $i $ th-Element von `paulis` und WHERE $N = $ ist `Length(paulis)` .</span><span class="sxs-lookup"><span data-stu-id="baae3-106">\begin{align} e^{i \pi k [P_0 \otimes P_1 \cdots P_{N-1}] / 2^n}, \end{align} where $P_i$ is the $i$th element of `paulis`, and where $N = $`Length(paulis)`.</span></span>

```qsharp
operation ExpFrac (paulis : Pauli[], numerator : Int, power : Int, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="baae3-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="baae3-107">Input</span></span>

### <a name="paulis--pauli"></a><span data-ttu-id="baae3-108">Paulis: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="baae3-108">paulis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="baae3-109">Array von Single-Qubit-Pauli-Werten, die die tensorflow-Produkt Faktoren für jedes Qubit angeben.</span><span class="sxs-lookup"><span data-stu-id="baae3-109">Array of single-qubit Pauli values indicating the tensor product factors on each qubit.</span></span>


### <a name="numerator--int"></a><span data-ttu-id="baae3-110">Zähler: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="baae3-110">numerator : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="baae3-111">Der Zähler ($k $) in der dyadic-Bruch Darstellung des Winkels, um den das Qubit-Register gedreht werden soll.</span><span class="sxs-lookup"><span data-stu-id="baae3-111">Numerator ($k$) in the dyadic fraction representation of the angle by which the qubit register is to be rotated.</span></span>


### <a name="power--int"></a><span data-ttu-id="baae3-112">Power: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="baae3-112">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="baae3-113">Potenz von zwei ($n $), die den Nenner des Winkels angibt, um den das Qubit-Register gedreht werden soll.</span><span class="sxs-lookup"><span data-stu-id="baae3-113">Power of two ($n$) specifying the denominator of the angle by which the qubit register is to be rotated.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="baae3-114">Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="baae3-114">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="baae3-115">Registrieren Sie sich, um die angegebene Drehung auf anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="baae3-115">Register to apply the given rotation to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="baae3-116">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="baae3-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>


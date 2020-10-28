---
uid: Microsoft.Quantum.Intrinsic.ExpFrac
title: Expfrac-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: ExpFrac
qsharp.summary: >-
  Applies the exponential of a multi-qubit Pauli operator with an argument given by a dyadic fraction.

  \begin{align} e^{i \pi k [P_0 \otimes P_1 \cdots P_{N-1}] / 2^n}, \end{align} where $P_i$ is the $i$th element of `paulis`, and where $N = $`Length(paulis)`.
ms.openlocfilehash: d11912a272387b087098f59e7ac071534b01c054
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702119"
---
# <a name="expfrac-operation"></a><span data-ttu-id="b5cac-102">Expfrac-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b5cac-102">ExpFrac operation</span></span>

<span data-ttu-id="b5cac-103">Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="b5cac-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="b5cac-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b5cac-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b5cac-105">Wendet den Exponentialwert eines multiqubit-Pauli-Operators mit einem Argument an, das von einem dyadic-Bruchteil angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b5cac-105">Applies the exponential of a multi-qubit Pauli operator with an argument given by a dyadic fraction.</span></span>

<span data-ttu-id="b5cac-106">\begin{align} e ^ {i \pi k [P_0 \otimes P_1 \cdots P_ {N-1}]/2 ^ N}, \end{align}, wobei $P _I $ das $i $ th-Element von `paulis` und WHERE $N = $ ist `Length(paulis)` .</span><span class="sxs-lookup"><span data-stu-id="b5cac-106">\begin{align} e^{i \pi k [P_0 \otimes P_1 \cdots P_{N-1}] / 2^n}, \end{align} where $P_i$ is the $i$th element of `paulis`, and where $N = $`Length(paulis)`.</span></span>

```qsharp
operation ExpFrac (paulis : Pauli[], numerator : Int, power : Int, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="b5cac-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b5cac-107">Input</span></span>

### <a name="paulis--pauli"></a><span data-ttu-id="b5cac-108">Paulis: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="b5cac-108">paulis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="b5cac-109">Array von Single-Qubit-Pauli-Werten, die die tensorflow-Produkt Faktoren für jedes Qubit angeben.</span><span class="sxs-lookup"><span data-stu-id="b5cac-109">Array of single-qubit Pauli values indicating the tensor product factors on each qubit.</span></span>


### <a name="numerator--int"></a><span data-ttu-id="b5cac-110">Zähler: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b5cac-110">numerator : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b5cac-111">Der Zähler ($k $) in der dyadic-Bruch Darstellung des Winkels, um den das Qubit-Register gedreht werden soll.</span><span class="sxs-lookup"><span data-stu-id="b5cac-111">Numerator ($k$) in the dyadic fraction representation of the angle by which the qubit register is to be rotated.</span></span>


### <a name="power--int"></a><span data-ttu-id="b5cac-112">Power: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b5cac-112">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b5cac-113">Potenz von zwei ($n $), die den Nenner des Winkels angibt, um den das Qubit-Register gedreht werden soll.</span><span class="sxs-lookup"><span data-stu-id="b5cac-113">Power of two ($n$) specifying the denominator of the angle by which the qubit register is to be rotated.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="b5cac-114">Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="b5cac-114">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="b5cac-115">Registrieren Sie sich, um die angegebene Drehung auf anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="b5cac-115">Register to apply the given rotation to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b5cac-116">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b5cac-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>


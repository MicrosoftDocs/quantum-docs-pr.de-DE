---
uid: Microsoft.Quantum.Intrinsic.Exp
title: Exp-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Exp
qsharp.summary: >-
  Applies the exponential of a multi-qubit Pauli operator.

  \begin{align} e^{i \theta [P_0 \otimes P_1 \cdots P_{N-1}]}, \end{align} where $P_i$ is the $i$th element of `paulis`, and where $N = $`Length(paulis)`.
ms.openlocfilehash: b923374a954f90aba2deaead79dd419fbf67fea3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702132"
---
# <a name="exp-operation"></a><span data-ttu-id="5e10b-102">Exp-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5e10b-102">Exp operation</span></span>

<span data-ttu-id="5e10b-103">Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="5e10b-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="5e10b-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5e10b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5e10b-105">Wendet den Exponentialwert eines multiqubit-Pauli-Operators an.</span><span class="sxs-lookup"><span data-stu-id="5e10b-105">Applies the exponential of a multi-qubit Pauli operator.</span></span>

<span data-ttu-id="5e10b-106">\begin{align} e ^ {i \orta [P_0 \otimes P_1 \cdots P_ {N-1}]}, \end{align}, wobei $P _I $ das $i $ th-Element von `paulis` und $N = $ ist `Length(paulis)` .</span><span class="sxs-lookup"><span data-stu-id="5e10b-106">\begin{align} e^{i \theta [P_0 \otimes P_1 \cdots P_{N-1}]}, \end{align} where $P_i$ is the $i$th element of `paulis`, and where $N = $`Length(paulis)`.</span></span>

```qsharp
operation Exp (paulis : Pauli[], theta : Double, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="5e10b-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5e10b-107">Input</span></span>

### <a name="paulis--pauli"></a><span data-ttu-id="5e10b-108">Paulis: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="5e10b-108">paulis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="5e10b-109">Array von Single-Qubit-Pauli-Werten, die die tensorflow-Produkt Faktoren für jedes Qubit angeben.</span><span class="sxs-lookup"><span data-stu-id="5e10b-109">Array of single-qubit Pauli values indicating the tensor product factors on each qubit.</span></span>


### <a name="theta--double"></a><span data-ttu-id="5e10b-110">-Ta: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="5e10b-110">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="5e10b-111">Der Winkel zum angegebenen multiqubit-Pauli-Operator, um den das Ziel Register gedreht werden soll.</span><span class="sxs-lookup"><span data-stu-id="5e10b-111">Angle about the given multi-qubit Pauli operator by which the target register is to be rotated.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="5e10b-112">Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="5e10b-112">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="5e10b-113">Registrieren Sie sich, um die angegebene Drehung auf anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="5e10b-113">Register to apply the given rotation to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5e10b-114">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5e10b-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>


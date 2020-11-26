---
uid: Microsoft.Quantum.Intrinsic.Exp
title: Exp-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Exp
qsharp.summary: >-
  Applies the exponential of a multi-qubit Pauli operator.

  \begin{align} e^{i \theta [P_0 \otimes P_1 \cdots P_{N-1}]}, \end{align} where $P_i$ is the $i$th element of `paulis`, and where $N = $`Length(paulis)`.
ms.openlocfilehash: 2eea29ec08260ea9cee1bafde80a0942e06f5abc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96212408"
---
# <a name="exp-operation"></a><span data-ttu-id="b2b6b-102">Exp-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b2b6b-102">Exp operation</span></span>

<span data-ttu-id="b2b6b-103">Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="b2b6b-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="b2b6b-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="b2b6b-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="b2b6b-105">Wendet den Exponentialwert eines multiqubit-Pauli-Operators an.</span><span class="sxs-lookup"><span data-stu-id="b2b6b-105">Applies the exponential of a multi-qubit Pauli operator.</span></span>

<span data-ttu-id="b2b6b-106">\begin{align} e ^ {i \orta [P_0 \otimes P_1 \cdots P_ {N-1}]}, \end{align}, wobei $P _I $ das $i $ th-Element von `paulis` und $N = $ ist `Length(paulis)` .</span><span class="sxs-lookup"><span data-stu-id="b2b6b-106">\begin{align} e^{i \theta [P_0 \otimes P_1 \cdots P_{N-1}]}, \end{align} where $P_i$ is the $i$th element of `paulis`, and where $N = $`Length(paulis)`.</span></span>

```qsharp
operation Exp (paulis : Pauli[], theta : Double, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="b2b6b-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b2b6b-107">Input</span></span>

### <a name="paulis--pauli"></a><span data-ttu-id="b2b6b-108">Paulis: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="b2b6b-108">paulis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="b2b6b-109">Array von Single-Qubit-Pauli-Werten, die die tensorflow-Produkt Faktoren für jedes Qubit angeben.</span><span class="sxs-lookup"><span data-stu-id="b2b6b-109">Array of single-qubit Pauli values indicating the tensor product factors on each qubit.</span></span>


### <a name="theta--double"></a><span data-ttu-id="b2b6b-110">-Ta: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="b2b6b-110">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="b2b6b-111">Der Winkel zum angegebenen multiqubit-Pauli-Operator, um den das Ziel Register gedreht werden soll.</span><span class="sxs-lookup"><span data-stu-id="b2b6b-111">Angle about the given multi-qubit Pauli operator by which the target register is to be rotated.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="b2b6b-112">Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="b2b6b-112">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="b2b6b-113">Registrieren Sie sich, um die angegebene Drehung auf anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="b2b6b-113">Register to apply the given rotation to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b2b6b-114">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b2b6b-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>


---
uid: Microsoft.Quantum.Intrinsic.Exp
title: Exp-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Exp
qsharp.summary: >-
  Applies the exponential of a multi-qubit Pauli operator.

  \begin{align} e^{i \theta [P_0 \otimes P_1 \cdots P_{N-1}]}, \end{align} where $P_i$ is the $i$th element of `paulis`, and where $N = $`Length(paulis)`.
ms.openlocfilehash: 7aa6974e83e917125b63ef91fb5c3b1238f6e856
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98819007"
---
# <a name="exp-operation"></a><span data-ttu-id="65a24-102">Exp-Vorgang</span><span class="sxs-lookup"><span data-stu-id="65a24-102">Exp operation</span></span>

<span data-ttu-id="65a24-103">Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="65a24-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="65a24-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="65a24-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="65a24-105">Wendet den Exponentialwert eines multiqubit-Pauli-Operators an.</span><span class="sxs-lookup"><span data-stu-id="65a24-105">Applies the exponential of a multi-qubit Pauli operator.</span></span>

<span data-ttu-id="65a24-106">\begin{align} e ^ {i \orta [P_0 \otimes P_1 \cdots P_ {N-1}]}, \end{align}, wobei $P _I $ das $i $ th-Element von `paulis` und $N = $ ist `Length(paulis)` .</span><span class="sxs-lookup"><span data-stu-id="65a24-106">\begin{align} e^{i \theta [P_0 \otimes P_1 \cdots P_{N-1}]}, \end{align} where $P_i$ is the $i$th element of `paulis`, and where $N = $`Length(paulis)`.</span></span>

```qsharp
operation Exp (paulis : Pauli[], theta : Double, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="65a24-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="65a24-107">Input</span></span>

### <a name="paulis--pauli"></a><span data-ttu-id="65a24-108">Paulis: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="65a24-108">paulis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="65a24-109">Array von Single-Qubit-Pauli-Werten, die die tensorflow-Produkt Faktoren für jedes Qubit angeben.</span><span class="sxs-lookup"><span data-stu-id="65a24-109">Array of single-qubit Pauli values indicating the tensor product factors on each qubit.</span></span>


### <a name="theta--double"></a><span data-ttu-id="65a24-110">-Ta: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="65a24-110">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="65a24-111">Der Winkel zum angegebenen multiqubit-Pauli-Operator, um den das Ziel Register gedreht werden soll.</span><span class="sxs-lookup"><span data-stu-id="65a24-111">Angle about the given multi-qubit Pauli operator by which the target register is to be rotated.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="65a24-112">Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="65a24-112">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="65a24-113">Registrieren Sie sich, um die angegebene Drehung auf anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="65a24-113">Register to apply the given rotation to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="65a24-114">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="65a24-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>


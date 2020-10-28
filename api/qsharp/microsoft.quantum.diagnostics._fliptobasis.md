---
uid: Microsoft.Quantum.Diagnostics._flipToBasis
title: _flipToBasis Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: _flipToBasis
qsharp.summary: >-
  Applies unitaries that map $\ket{0}\otimes\cdots\ket{0}$ to $\ket{\psi_0} \otimes \ket{\psi_{n - 1}}$, where $\ket{\psi_k}$ depends on `basis[k]`.

  The correspondence between value of `basis[k]` and $\ket{\psi_k}$ is the following:

  - `basis[k]=0` $\rightarrow \ket{0}$. - `basis[k]=1` $\rightarrow \ket{1}$. - `basis[k]=2` $\rightarrow \ket{+}$. - `basis[k]=3` $\rightarrow \ket{i}$ ( +1 eigenstate of Pauli Y ).
ms.openlocfilehash: e074ed2ae259f6aef49a8d327ce518a9e2caebfa
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702828"
---
# <a name="_fliptobasis-operation"></a><span data-ttu-id="5ecb5-102">_flipToBasis Vorgang</span><span class="sxs-lookup"><span data-stu-id="5ecb5-102">_flipToBasis operation</span></span>

<span data-ttu-id="5ecb5-103">Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="5ecb5-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="5ecb5-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5ecb5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5ecb5-105">Wendet die unimaps an, die $ \ket {0} \otimes\cdoz\ket {0} $ zu $ \ket{\ psi_0} \otimes \ket{\ psi_ {n-1}} $ zuordnen, wobei $ \ket{\ psi_k} $ von abhängt `basis[k]` .</span><span class="sxs-lookup"><span data-stu-id="5ecb5-105">Applies unitaries that map $\ket{0}\otimes\cdots\ket{0}$ to $\ket{\psi_0} \otimes \ket{\psi_{n - 1}}$, where $\ket{\psi_k}$ depends on `basis[k]`.</span></span>

<span data-ttu-id="5ecb5-106">Die Entsprechung zwischen Wert `basis[k]` und $ \ket{\ psi_k} $ lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5ecb5-106">The correspondence between value of `basis[k]` and $\ket{\psi_k}$ is the following:</span></span>

- <span data-ttu-id="5ecb5-107">`basis[k]=0` $ \rightarrow \ket {0} $.</span><span class="sxs-lookup"><span data-stu-id="5ecb5-107">`basis[k]=0` $\rightarrow \ket{0}$.</span></span>
- <span data-ttu-id="5ecb5-108">`basis[k]=1` $ \rightarrow \ket {1} $.</span><span class="sxs-lookup"><span data-stu-id="5ecb5-108">`basis[k]=1` $\rightarrow \ket{1}$.</span></span>
- <span data-ttu-id="5ecb5-109">`basis[k]=2` $ \rightarrow \ket{+} $.</span><span class="sxs-lookup"><span data-stu-id="5ecb5-109">`basis[k]=2` $\rightarrow \ket{+}$.</span></span>
- <span data-ttu-id="5ecb5-110">`basis[k]=3` $ \rightarrow \ket{i} $ (+ 1 eigen Status von Pauli Y).</span><span class="sxs-lookup"><span data-stu-id="5ecb5-110">`basis[k]=3` $\rightarrow \ket{i}$ ( +1 eigenstate of Pauli Y ).</span></span>

```qsharp
operation _flipToBasis (basis : Int[], qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="5ecb5-111">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5ecb5-111">Input</span></span>

### <a name="basis--int"></a><span data-ttu-id="5ecb5-112">Basis: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="5ecb5-112">basis : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="5ecb5-113">Array von Single-Qubit-Basis-IDs (0 <= ID <= 3), eine für jedes Element von Qubits.</span><span class="sxs-lookup"><span data-stu-id="5ecb5-113">Array of single-qubit basis state IDs (0 <= id <= 3), one for each element of qubits.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="5ecb5-114">Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="5ecb5-114">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="5ecb5-115">Das zu verwendende Qubit.</span><span class="sxs-lookup"><span data-stu-id="5ecb5-115">Qubit to be operated on.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5ecb5-116">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5ecb5-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>


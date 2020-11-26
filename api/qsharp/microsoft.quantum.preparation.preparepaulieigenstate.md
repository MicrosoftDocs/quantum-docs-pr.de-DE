---
uid: Microsoft.Quantum.Preparation.PreparePauliEigenstate
title: Preparepaulieigen State-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PreparePauliEigenstate
qsharp.summary: Prepares a qubit in the positive eigenstate of a given Pauli operator. If the identity operator is given, then the qubit is prepared in the maximally mixed state.
ms.openlocfilehash: b24852bb3a455a9fe04b3535156d0c3dfb1a7d12
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193691"
---
# <a name="preparepaulieigenstate-operation"></a><span data-ttu-id="14e2f-102">Preparepaulieigen State-Vorgang</span><span class="sxs-lookup"><span data-stu-id="14e2f-102">PreparePauliEigenstate operation</span></span>

<span data-ttu-id="14e2f-103">Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="14e2f-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="14e2f-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="14e2f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="14e2f-105">Bereitet ein Qubit im positiven eigen Zustand eines angegebenen Pauli-Operators vor.</span><span class="sxs-lookup"><span data-stu-id="14e2f-105">Prepares a qubit in the positive eigenstate of a given Pauli operator.</span></span>
<span data-ttu-id="14e2f-106">Wenn der Identity-Operator angegeben ist, wird das Qubit im Status "in maximalgemischter Form" vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="14e2f-106">If the identity operator is given, then the qubit is prepared in the maximally mixed state.</span></span>

```qsharp
operation PreparePauliEigenstate (basis : Pauli, qubit : Qubit) : Unit
```


## <a name="description"></a><span data-ttu-id="14e2f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="14e2f-107">Description</span></span>

<span data-ttu-id="14e2f-108">Wenn sich das Qubit anfänglich im $ \ket {0} $-Zustand befunden hat, bereitet dieser Vorgang das Qubit im $ + $1-eigen Zustand eines angegebenen Pauli-Operators bzw `PauliI` . für im Status "maximisch Mixed" (siehe <xref:microsoft.quantum.preparation.preparesinglequbitidentity> ) vor.</span><span class="sxs-lookup"><span data-stu-id="14e2f-108">If the qubit was initially in the $\ket{0}$ state, this operation prepares the qubit in the $+1$ eigenstate of a given Pauli operator, or, for `PauliI`, in the maximally mixed state instead (see <xref:microsoft.quantum.preparation.preparesinglequbitidentity>).</span></span>

<span data-ttu-id="14e2f-109">Wenn sich das Qubit in einem anderen Zustand als $ \ket {0} $ befunden hat, wendet dieser Vorgang die folgenden Gates an: $H $ for `PauliX` , $HS $ for `PauliY` , $I $ for `PauliZ` und <xref:microsoft.quantum.preparation.preparesinglequbitidentity> for `PauliI` .</span><span class="sxs-lookup"><span data-stu-id="14e2f-109">If the qubit was in a state other than $\ket{0}$, this operation applies the following gates: $H$ for `PauliX`, $HS$ for `PauliY`, $I$ for `PauliZ` and <xref:microsoft.quantum.preparation.preparesinglequbitidentity> for `PauliI`.</span></span>

## <a name="input"></a><span data-ttu-id="14e2f-110">Eingabe</span><span class="sxs-lookup"><span data-stu-id="14e2f-110">Input</span></span>

### <a name="basis--pauli"></a><span data-ttu-id="14e2f-111">Basis: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="14e2f-111">basis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="14e2f-112">Ein Pauli-Operator $P $.</span><span class="sxs-lookup"><span data-stu-id="14e2f-112">A Pauli operator $P$.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="14e2f-113">Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="14e2f-113">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="14e2f-114">Ein Qubit, das vorbereitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="14e2f-114">A qubit to be prepared.</span></span>



## <a name="output--unit"></a><span data-ttu-id="14e2f-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="14e2f-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>


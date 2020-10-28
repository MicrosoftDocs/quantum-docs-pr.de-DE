---
uid: Microsoft.Quantum.Preparation.PrepareQubit
title: Preparequbit-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareQubit
qsharp.summary: >-
  Prepares a qubit in the +1 (`Zero`) eigenstate of the given Pauli operator. If the identity operator is given, then the qubit is prepared in the maximally mixed state.

  If the qubit was initially in the $\ket{0}$ state, this operation prepares the qubit in the $+1$ eigenstate of a given Pauli operator, or, for `PauliI`, in the maximally mixed state instead (see <xref:microsoft.quantum.preparation.preparesinglequbitidentity>).

  If the qubit was in a state other than $\ket{0}$, this operation applies the following gates: $H$ for `PauliX`, $HS$ for `PauliY`, $I$ for `PauliZ` and <xref:microsoft.quantum.preparation.preparesinglequbitidentity> for `PauliI`.
ms.openlocfilehash: 5f42bf26a8f9638ea88c035a18846050c3776b45
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723004"
---
# <a name="preparequbit-operation"></a><span data-ttu-id="e1707-102">Preparequbit-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e1707-102">PrepareQubit operation</span></span>

<span data-ttu-id="e1707-103">Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="e1707-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="e1707-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e1707-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e1707-105">Bereitet ein Qubit im + 1 ( `Zero` )-eigen Zustand des angegebenen Pauli-Operators vor.</span><span class="sxs-lookup"><span data-stu-id="e1707-105">Prepares a qubit in the +1 (`Zero`) eigenstate of the given Pauli operator.</span></span>
<span data-ttu-id="e1707-106">Wenn der Identity-Operator angegeben ist, wird das Qubit im Status "in maximalgemischter Form" vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="e1707-106">If the identity operator is given, then the qubit is prepared in the maximally mixed state.</span></span>

<span data-ttu-id="e1707-107">Wenn sich das Qubit anfänglich im $ \ket {0} $-Zustand befunden hat, bereitet dieser Vorgang das Qubit im $ + $1-eigen Zustand eines angegebenen Pauli-Operators bzw `PauliI` . für im Status "maximisch Mixed" (siehe <xref:microsoft.quantum.preparation.preparesinglequbitidentity> ) vor.</span><span class="sxs-lookup"><span data-stu-id="e1707-107">If the qubit was initially in the $\ket{0}$ state, this operation prepares the qubit in the $+1$ eigenstate of a given Pauli operator, or, for `PauliI`, in the maximally mixed state instead (see <xref:microsoft.quantum.preparation.preparesinglequbitidentity>).</span></span>

<span data-ttu-id="e1707-108">Wenn sich das Qubit in einem anderen Zustand als $ \ket {0} $ befunden hat, wendet dieser Vorgang die folgenden Gates an: $H $ for `PauliX` , $HS $ for `PauliY` , $I $ for `PauliZ` und <xref:microsoft.quantum.preparation.preparesinglequbitidentity> for `PauliI` .</span><span class="sxs-lookup"><span data-stu-id="e1707-108">If the qubit was in a state other than $\ket{0}$, this operation applies the following gates: $H$ for `PauliX`, $HS$ for `PauliY`, $I$ for `PauliZ` and <xref:microsoft.quantum.preparation.preparesinglequbitidentity> for `PauliI`.</span></span>

```qsharp
operation PrepareQubit (basis : Pauli, qubit : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="e1707-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e1707-109">Input</span></span>

### <a name="basis--pauli"></a><span data-ttu-id="e1707-110">Basis: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="e1707-110">basis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="e1707-111">Ein Pauli-Operator $P $.</span><span class="sxs-lookup"><span data-stu-id="e1707-111">A Pauli operator $P$.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="e1707-112">Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="e1707-112">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="e1707-113">Ein Qubit, das vorbereitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e1707-113">A qubit to be prepared.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e1707-114">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e1707-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>


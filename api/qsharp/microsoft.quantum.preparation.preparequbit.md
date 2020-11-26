---
uid: Microsoft.Quantum.Preparation.PrepareQubit
title: Preparequbit-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareQubit
qsharp.summary: >-
  > [!WARNING]

  > PrepareQubit has been deprecated. Please use <xref:Microsoft.Quantum.Preparation.PreparePauliEigenstate> instead.


  Prepares a qubit in the +1 (`Zero`) eigenstate of the given Pauli operator. If the identity operator is given, then the qubit is prepared in the maximally mixed state.

  If the qubit was initially in the $\ket{0}$ state, this operation prepares the qubit in the $+1$ eigenstate of a given Pauli operator, or, for `PauliI`, in the maximally mixed state instead (see <xref:microsoft.quantum.preparation.preparesinglequbitidentity>).

  If the qubit was in a state other than $\ket{0}$, this operation applies the following gates: $H$ for `PauliX`, $HS$ for `PauliY`, $I$ for `PauliZ` and <xref:microsoft.quantum.preparation.preparesinglequbitidentity> for `PauliI`.
ms.openlocfilehash: 84674d70d6a038ceaf1c637b22afa1b724d90795
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193521"
---
# <a name="preparequbit-operation"></a><span data-ttu-id="2b591-102">Preparequbit-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2b591-102">PrepareQubit operation</span></span>

<span data-ttu-id="2b591-103">Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="2b591-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="2b591-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2b591-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="2b591-105">Preparequbit ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="2b591-105">PrepareQubit has been deprecated.</span></span> <span data-ttu-id="2b591-106">Verwenden Sie stattdessen <xref:Microsoft.Quantum.Preparation.PreparePauliEigenstate>.</span><span class="sxs-lookup"><span data-stu-id="2b591-106">Please use <xref:Microsoft.Quantum.Preparation.PreparePauliEigenstate> instead.</span></span>

<span data-ttu-id="2b591-107">Bereitet ein Qubit im + 1 ( `Zero` )-eigen Zustand des angegebenen Pauli-Operators vor.</span><span class="sxs-lookup"><span data-stu-id="2b591-107">Prepares a qubit in the +1 (`Zero`) eigenstate of the given Pauli operator.</span></span>
<span data-ttu-id="2b591-108">Wenn der Identity-Operator angegeben ist, wird das Qubit im Status "in maximalgemischter Form" vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="2b591-108">If the identity operator is given, then the qubit is prepared in the maximally mixed state.</span></span>

<span data-ttu-id="2b591-109">Wenn sich das Qubit anfänglich im $ \ket {0} $-Zustand befunden hat, bereitet dieser Vorgang das Qubit im $ + $1-eigen Zustand eines angegebenen Pauli-Operators bzw `PauliI` . für im Status "maximisch Mixed" (siehe <xref:microsoft.quantum.preparation.preparesinglequbitidentity> ) vor.</span><span class="sxs-lookup"><span data-stu-id="2b591-109">If the qubit was initially in the $\ket{0}$ state, this operation prepares the qubit in the $+1$ eigenstate of a given Pauli operator, or, for `PauliI`, in the maximally mixed state instead (see <xref:microsoft.quantum.preparation.preparesinglequbitidentity>).</span></span>

<span data-ttu-id="2b591-110">Wenn sich das Qubit in einem anderen Zustand als $ \ket {0} $ befunden hat, wendet dieser Vorgang die folgenden Gates an: $H $ for `PauliX` , $HS $ for `PauliY` , $I $ for `PauliZ` und <xref:microsoft.quantum.preparation.preparesinglequbitidentity> for `PauliI` .</span><span class="sxs-lookup"><span data-stu-id="2b591-110">If the qubit was in a state other than $\ket{0}$, this operation applies the following gates: $H$ for `PauliX`, $HS$ for `PauliY`, $I$ for `PauliZ` and <xref:microsoft.quantum.preparation.preparesinglequbitidentity> for `PauliI`.</span></span>

```qsharp
operation PrepareQubit (basis : Pauli, qubit : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="2b591-111">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2b591-111">Input</span></span>

### <a name="basis--pauli"></a><span data-ttu-id="2b591-112">Basis: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="2b591-112">basis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="2b591-113">Ein Pauli-Operator $P $.</span><span class="sxs-lookup"><span data-stu-id="2b591-113">A Pauli operator $P$.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="2b591-114">Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="2b591-114">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="2b591-115">Ein Qubit, das vorbereitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2b591-115">A qubit to be prepared.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2b591-116">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2b591-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>


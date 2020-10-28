---
uid: Microsoft.Quantum.Arithmetic.AssertProbInt
title: Assertprobint-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertProbInt
qsharp.summary: Asserts that the probability of a specific state of a quantum register has the expected value.
ms.openlocfilehash: a8e4217e18528adc0aa9923f1c0dcfb59e1d2488
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707439"
---
# <a name="assertprobint-operation"></a><span data-ttu-id="0ee15-102">Assertprobint-Vorgang</span><span class="sxs-lookup"><span data-stu-id="0ee15-102">AssertProbInt operation</span></span>

<span data-ttu-id="0ee15-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="0ee15-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="0ee15-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0ee15-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0ee15-105">Bestätigt, dass die Wahrscheinlichkeit eines bestimmten Zustands eines Quantum-Register über den erwarteten Wert verfügt.</span><span class="sxs-lookup"><span data-stu-id="0ee15-105">Asserts that the probability of a specific state of a quantum register has the expected value.</span></span>

```qsharp
operation AssertProbInt (stateIndex : Int, expected : Double, qubits : Microsoft.Quantum.Arithmetic.LittleEndian, tolerance : Double) : Unit
```


## <a name="description"></a><span data-ttu-id="0ee15-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0ee15-106">Description</span></span>

<span data-ttu-id="0ee15-107">Bestätigt bei einem $n $-Qubit-Quantum-Status $ \ket{\psi} = \sum ^ {2 ^ n-1} _ {j = 0} \ alpha_j \ket{j} $, dass die Wahrscheinlichkeit $ | \ alpha_j | ^ 2 $ des durch $j $ indizierten Zustands $ \ket{j} $ den erwarteten Wert hat.</span><span class="sxs-lookup"><span data-stu-id="0ee15-107">Given an $n$-qubit quantum state $\ket{\psi}=\sum^{2^n-1}_{j=0}\alpha_j \ket{j}$, asserts that the probability $|\alpha_j|^2$ of the state $\ket{j}$ indexed by $j$ has the expected value.</span></span>

## <a name="input"></a><span data-ttu-id="0ee15-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0ee15-108">Input</span></span>

### <a name="stateindex--int"></a><span data-ttu-id="0ee15-109">Status Index: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0ee15-109">stateIndex : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0ee15-110">Der Index $j $ des Zustands $ \ket{j} $, der durch ein `LittleEndian` Register dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="0ee15-110">The index $j$ of the state $\ket{j}$ represented by a `LittleEndian` register.</span></span>


### <a name="expected--double"></a><span data-ttu-id="0ee15-111">erwartet: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="0ee15-111">expected : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="0ee15-112">Der erwartete Wert von $ | \ alpha_j | ^ 2 $.</span><span class="sxs-lookup"><span data-stu-id="0ee15-112">The expected value of $|\alpha_j|^2$.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="0ee15-113">Qubits: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="0ee15-113">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="0ee15-114">Das Qubit-Register, das $ \ket{\psi} $ im Little-Endian-Format speichert.</span><span class="sxs-lookup"><span data-stu-id="0ee15-114">The qubit register that stores $\ket{\psi}$ in little-endian format.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="0ee15-115">Toleranz: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="0ee15-115">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="0ee15-116">Absolute Toleranz für den Unterschied zwischen tatsächlichem und erwartetem Verhalten.</span><span class="sxs-lookup"><span data-stu-id="0ee15-116">Absolute tolerance on the difference between actual and expected.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0ee15-117">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0ee15-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>


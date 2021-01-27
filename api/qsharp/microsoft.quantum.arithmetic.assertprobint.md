---
uid: Microsoft.Quantum.Arithmetic.AssertProbInt
title: Assertprobint-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertProbInt
qsharp.summary: Asserts that the probability of a specific state of a quantum register has the expected value.
ms.openlocfilehash: 85ff04bbad9dc2ed0f803db65508fdfbb0d22c56
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843404"
---
# <a name="assertprobint-operation"></a><span data-ttu-id="5fb1e-102">Assertprobint-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5fb1e-102">AssertProbInt operation</span></span>

<span data-ttu-id="5fb1e-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="5fb1e-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="5fb1e-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5fb1e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5fb1e-105">Bestätigt, dass die Wahrscheinlichkeit eines bestimmten Zustands eines Quantum-Register über den erwarteten Wert verfügt.</span><span class="sxs-lookup"><span data-stu-id="5fb1e-105">Asserts that the probability of a specific state of a quantum register has the expected value.</span></span>

```qsharp
operation AssertProbInt (stateIndex : Int, expected : Double, qubits : Microsoft.Quantum.Arithmetic.LittleEndian, tolerance : Double) : Unit
```


## <a name="description"></a><span data-ttu-id="5fb1e-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5fb1e-106">Description</span></span>

<span data-ttu-id="5fb1e-107">Bestätigt bei einem $n $-Qubit-Quantum-Status $ \ket{\psi} = \sum ^ {2 ^ n-1} _ {j = 0} \ alpha_j \ket{j} $, dass die Wahrscheinlichkeit $ | \ alpha_j | ^ 2 $ des durch $j $ indizierten Zustands $ \ket{j} $ den erwarteten Wert hat.</span><span class="sxs-lookup"><span data-stu-id="5fb1e-107">Given an $n$-qubit quantum state $\ket{\psi}=\sum^{2^n-1}_{j=0}\alpha_j \ket{j}$, asserts that the probability $|\alpha_j|^2$ of the state $\ket{j}$ indexed by $j$ has the expected value.</span></span>

## <a name="input"></a><span data-ttu-id="5fb1e-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5fb1e-108">Input</span></span>

### <a name="stateindex--int"></a><span data-ttu-id="5fb1e-109">Status Index: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5fb1e-109">stateIndex : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5fb1e-110">Der Index $j $ des Zustands $ \ket{j} $, der durch ein `LittleEndian` Register dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="5fb1e-110">The index $j$ of the state $\ket{j}$ represented by a `LittleEndian` register.</span></span>


### <a name="expected--double"></a><span data-ttu-id="5fb1e-111">erwartet: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="5fb1e-111">expected : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="5fb1e-112">Der erwartete Wert von $ | \ alpha_j | ^ 2 $.</span><span class="sxs-lookup"><span data-stu-id="5fb1e-112">The expected value of $|\alpha_j|^2$.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="5fb1e-113">Qubits: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="5fb1e-113">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="5fb1e-114">Das Qubit-Register, das $ \ket{\psi} $ im Little-Endian-Format speichert.</span><span class="sxs-lookup"><span data-stu-id="5fb1e-114">The qubit register that stores $\ket{\psi}$ in little-endian format.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="5fb1e-115">Toleranz: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="5fb1e-115">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="5fb1e-116">Absolute Toleranz für den Unterschied zwischen tatsächlichem und erwartetem Verhalten.</span><span class="sxs-lookup"><span data-stu-id="5fb1e-116">Absolute tolerance on the difference between actual and expected.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5fb1e-117">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5fb1e-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="5fb1e-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5fb1e-118">Example</span></span>

<span data-ttu-id="5fb1e-119">Angenommen, das `qubits` Register codiert einen 3-Qubit-Quantum-Status $ \ket{\psi} = \ sqrt {1/8} \ Ket {0} + \ sqrt {7/8} \ Ket {6} $ im Little-Endian-Format.</span><span class="sxs-lookup"><span data-stu-id="5fb1e-119">Suppose that the `qubits` register encodes a 3-qubit quantum state $\ket{\psi}=\sqrt{1/8}\ket{0}+\sqrt{7/8}\ket{6}$ in little-endian format.</span></span>
<span data-ttu-id="5fb1e-120">Dies bedeutet, dass die Zahl "$ \ket {0} \equiv\ket {0} \ket {0} \ket {0} $" und "$ \ket {6} \equiv\ket {0} \ket {1} \ket {1} $" lautet.</span><span class="sxs-lookup"><span data-stu-id="5fb1e-120">This means that the number states $\ket{0}\equiv\ket{0}\ket{0}\ket{0}$ and $\ket{6}\equiv\ket{0}\ket{1}\ket{1}$.</span></span> <span data-ttu-id="5fb1e-121">Die folgenden Bestätigungen werden erfolgreich ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="5fb1e-121">Then the following asserts succeed:</span></span>

```qsharp
AssertProbInt(0, 0.125, qubits, 10e-10);
AssertProbInt(6, 0.875, qubits, 10e-10);
```
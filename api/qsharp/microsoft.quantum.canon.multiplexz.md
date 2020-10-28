---
uid: Microsoft.Quantum.Canon.MultiplexZ
title: Multiplexz-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexZ
qsharp.summary: Applies a Pauli Z rotation conditioned on an array of qubits.
ms.openlocfilehash: f7b1973e18ad396ebe892ad63ae47374a7cafbd5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703956"
---
# <a name="multiplexz-operation"></a><span data-ttu-id="59ad3-102">Multiplexz-Vorgang</span><span class="sxs-lookup"><span data-stu-id="59ad3-102">MultiplexZ operation</span></span>

<span data-ttu-id="59ad3-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="59ad3-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="59ad3-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="59ad3-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="59ad3-105">Wendet eine Pauli Z-Drehung an, die auf ein Array von Qubits bedingt ist.</span><span class="sxs-lookup"><span data-stu-id="59ad3-105">Applies a Pauli Z rotation conditioned on an array of qubits.</span></span>

```qsharp
operation MultiplexZ (coefficients : Double[], control : Microsoft.Quantum.Arithmetic.LittleEndian, target : Qubit) : Unit
```


## <a name="description"></a><span data-ttu-id="59ad3-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="59ad3-106">Description</span></span>

<span data-ttu-id="59ad3-107">Dadurch wird der Multiplikations gesteuerte einheitliche Vorgang angewendet, der die Drehung durch den Winkel $ \ theta_j $ um einen Single-Qubit-Pauli-Operator $Z $ durchführt, wenn er vom $n $-Qubit-Zahlen Status $ \ket{j} $ gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="59ad3-107">This applies the multiply controlled unitary operation that performs rotations by angle $\theta_j$ about single-qubit Pauli operator $Z$ when controlled by the $n$-qubit number state $\ket{j}$.</span></span>
<span data-ttu-id="59ad3-108">Insbesondere kann dieser Vorgang durch die einheitliche</span><span class="sxs-lookup"><span data-stu-id="59ad3-108">In particular, this operation can be represented by the unitary</span></span>

<span data-ttu-id="59ad3-109">$ $ \begin{align} U = \sum ^ {2 ^ n-1} _ {j = 0} \ket{j}\bra{j} \otimes e ^ {i Z \ theta_j}.</span><span class="sxs-lookup"><span data-stu-id="59ad3-109">$$ \begin{align} U = \sum^{2^n-1}_{j=0} \ket{j}\bra{j} \otimes e^{i Z \theta_j}.</span></span>
<span data-ttu-id="59ad3-110">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="59ad3-110">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="59ad3-111">Eingabe</span><span class="sxs-lookup"><span data-stu-id="59ad3-111">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="59ad3-112">Koeffizienten: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="59ad3-112">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="59ad3-113">Array von bis zu $2 ^ n $ Koeffizienten $ \ theta_j $.</span><span class="sxs-lookup"><span data-stu-id="59ad3-113">Array of up to $2^n$ coefficients $\theta_j$.</span></span> <span data-ttu-id="59ad3-114">Der $j $ Th-Koeffizienten indiziert den im Little-Endian-Format codierten Zahlen Status $ \ket{j} $.</span><span class="sxs-lookup"><span data-stu-id="59ad3-114">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="control--littleendian"></a><span data-ttu-id="59ad3-115">Control: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="59ad3-115">control : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="59ad3-116">$n $-Qubit-Steuerelement Register, das die Anzahl der Zustände $ \ket{j} $ im Little-Endian-Format codiert.</span><span class="sxs-lookup"><span data-stu-id="59ad3-116">$n$-qubit control register that encodes number states $\ket{j}$ in little-endian format.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="59ad3-117">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="59ad3-117">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="59ad3-118">Einzelnes Qubit-Register, das durch $e ^ {i P \ theta_j} $ gedreht wird.</span><span class="sxs-lookup"><span data-stu-id="59ad3-118">Single qubit register that is rotated by $e^{i P \theta_j}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="59ad3-119">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="59ad3-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="59ad3-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="59ad3-120">Remarks</span></span>

<span data-ttu-id="59ad3-121">`coefficients` wird mit Elementen $ \ theta_j = $0,0 aufgefüllt, wenn weniger als $2 ^ n $ angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="59ad3-121">`coefficients` will be padded with elements $\theta_j = 0.0$ if fewer than $2^n$ are specified.</span></span>

## <a name="references"></a><span data-ttu-id="59ad3-122">Referenzen</span><span class="sxs-lookup"><span data-stu-id="59ad3-122">References</span></span>

- <span data-ttu-id="59ad3-123">Synthese von Quantum Logic-Leitungen Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span><span class="sxs-lookup"><span data-stu-id="59ad3-123">Synthesis of Quantum Logic Circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span></span>

## <a name="see-also"></a><span data-ttu-id="59ad3-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="59ad3-124">See Also</span></span>

- [<span data-ttu-id="59ad3-125">Microsoft. Quantum. Canon. ungefähre atelymultiplexz</span><span class="sxs-lookup"><span data-stu-id="59ad3-125">Microsoft.Quantum.Canon.ApproximatelyMultiplexZ</span></span>](xref:Microsoft.Quantum.Canon.ApproximatelyMultiplexZ)
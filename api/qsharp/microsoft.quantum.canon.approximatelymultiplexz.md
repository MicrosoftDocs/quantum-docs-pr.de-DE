---
uid: Microsoft.Quantum.Canon.ApproximatelyMultiplexZ
title: Ungefäatelymultiplexz-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApproximatelyMultiplexZ
qsharp.summary: Applies a Pauli Z rotation conditioned on an array of qubits, truncating small rotation angles according to a given tolerance.
ms.openlocfilehash: b69b4de62241a7d16c2f07449115f864defda45d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841089"
---
# <a name="approximatelymultiplexz-operation"></a><span data-ttu-id="9f052-102">Ungefäatelymultiplexz-Vorgang</span><span class="sxs-lookup"><span data-stu-id="9f052-102">ApproximatelyMultiplexZ operation</span></span>

<span data-ttu-id="9f052-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="9f052-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="9f052-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9f052-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9f052-105">Wendet eine Pauli Z-Drehung an, die auf ein Array von Qubits bedingt ist, wobei kleine Drehwinkel entsprechend einer gegebenen Toleranz abgeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="9f052-105">Applies a Pauli Z rotation conditioned on an array of qubits, truncating small rotation angles according to a given tolerance.</span></span>

```qsharp
operation ApproximatelyMultiplexZ (tolerance : Double, coefficients : Double[], control : Microsoft.Quantum.Arithmetic.LittleEndian, target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="9f052-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9f052-106">Description</span></span>

<span data-ttu-id="9f052-107">Dadurch wird der Multiplikations gesteuerte einheitliche Vorgang angewendet, der die Drehung durch den Winkel $ \ theta_j $ um einen Single-Qubit-Pauli-Operator $Z $ durchführt, wenn er vom $n $-Qubit-Zahlen Status $ \ket{j} $ gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="9f052-107">This applies the multiply controlled unitary operation that performs rotations by angle $\theta_j$ about single-qubit Pauli operator $Z$ when controlled by the $n$-qubit number state $\ket{j}$.</span></span>
<span data-ttu-id="9f052-108">Insbesondere kann dieser Vorgang durch die einheitliche</span><span class="sxs-lookup"><span data-stu-id="9f052-108">In particular, this operation can be represented by the unitary</span></span>

<span data-ttu-id="9f052-109">$ $ \begin{align} U = \sum ^ {2 ^ n-1} _ {j = 0} \ket{j}\bra{j} \otimes e ^ {i Z \ theta_j}.</span><span class="sxs-lookup"><span data-stu-id="9f052-109">$$ \begin{align} U = \sum^{2^n-1}_{j=0} \ket{j}\bra{j} \otimes e^{i Z \theta_j}.</span></span>
<span data-ttu-id="9f052-110">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="9f052-110">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="9f052-111">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9f052-111">Input</span></span>

### <a name="tolerance--double"></a><span data-ttu-id="9f052-112">Toleranz: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="9f052-112">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="9f052-113">Eine Toleranz, unter der kleine Koeffizienten abgeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="9f052-113">A tolerance below which small coefficients are truncated.</span></span>


### <a name="coefficients--double"></a><span data-ttu-id="9f052-114">Koeffizienten: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="9f052-114">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="9f052-115">Array von bis zu $2 ^ n $ Koeffizienten $ \ theta_j $.</span><span class="sxs-lookup"><span data-stu-id="9f052-115">Array of up to $2^n$ coefficients $\theta_j$.</span></span> <span data-ttu-id="9f052-116">Der $j $ Th-Koeffizienten indiziert den im Little-Endian-Format codierten Zahlen Status $ \ket{j} $.</span><span class="sxs-lookup"><span data-stu-id="9f052-116">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="control--littleendian"></a><span data-ttu-id="9f052-117">Control: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="9f052-117">control : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="9f052-118">$n $-Qubit-Steuerelement Register, das die Anzahl der Zustände $ \ket{j} $ im Little-Endian-Format codiert.</span><span class="sxs-lookup"><span data-stu-id="9f052-118">$n$-qubit control register that encodes number states $\ket{j}$ in little-endian format.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="9f052-119">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="9f052-119">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="9f052-120">Einzelnes Qubit-Register, das durch $e ^ {i P \ theta_j} $ gedreht wird.</span><span class="sxs-lookup"><span data-stu-id="9f052-120">Single qubit register that is rotated by $e^{i P \theta_j}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9f052-121">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9f052-121">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="9f052-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9f052-122">Remarks</span></span>

<span data-ttu-id="9f052-123">`coefficients` wird mit Elementen $ \ theta_j = $0,0 aufgefüllt, wenn weniger als $2 ^ n $ angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9f052-123">`coefficients` will be padded with elements $\theta_j = 0.0$ if fewer than $2^n$ are specified.</span></span>

## <a name="references"></a><span data-ttu-id="9f052-124">References</span><span class="sxs-lookup"><span data-stu-id="9f052-124">References</span></span>

- <span data-ttu-id="9f052-125">Synthese von Quantum Logic-Leitungen Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span><span class="sxs-lookup"><span data-stu-id="9f052-125">Synthesis of Quantum Logic Circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span></span>

## <a name="see-also"></a><span data-ttu-id="9f052-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9f052-126">See Also</span></span>

- [<span data-ttu-id="9f052-127">Microsoft. Quantum. Canon. multiplexz</span><span class="sxs-lookup"><span data-stu-id="9f052-127">Microsoft.Quantum.Canon.MultiplexZ</span></span>](xref:Microsoft.Quantum.Canon.MultiplexZ)
---
uid: Microsoft.Quantum.Canon.MultiplexPauli
title: Multiplexpauli-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexPauli
qsharp.summary: Applies a Pauli rotation conditioned on an array of qubits.
ms.openlocfilehash: c29f7efa6b10835ce41ca4c535ec1371ac38ab63
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96206032"
---
# <a name="multiplexpauli-operation"></a><span data-ttu-id="5b8da-102">Multiplexpauli-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5b8da-102">MultiplexPauli operation</span></span>

<span data-ttu-id="5b8da-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5b8da-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5b8da-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5b8da-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5b8da-105">Wendet eine für ein Array von Qubits bedingte Pauli-Rotation an.</span><span class="sxs-lookup"><span data-stu-id="5b8da-105">Applies a Pauli rotation conditioned on an array of qubits.</span></span>

```qsharp
operation MultiplexPauli (coefficients : Double[], pauli : Pauli, control : Microsoft.Quantum.Arithmetic.LittleEndian, target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="5b8da-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5b8da-106">Description</span></span>

<span data-ttu-id="5b8da-107">Dadurch wird ein mehrfach gesteuerter einheitlicher Vorgang angewendet, bei dem die Drehung um den Winkel $ \ theta_j $ um einen Single-Qubit-Pauli-Operator $P $ durchführt, wenn er vom $n $-Qubit-Zahlen Status $ \ket{j} $ gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="5b8da-107">This applies a multiply controlled unitary operation that performs rotations by angle $\theta_j$ about single-qubit Pauli operator $P$ when controlled by the $n$-qubit number state $\ket{j}$.</span></span>
<span data-ttu-id="5b8da-108">Insbesondere wird die Aktion dieses Vorgangs durch die einheitliche</span><span class="sxs-lookup"><span data-stu-id="5b8da-108">In particular, the action of this operation is represented by the unitary</span></span>

<span data-ttu-id="5b8da-109">$ $ \begin{align} U = \sum ^ {2 ^ n-1} _ {j = 0} \ket{j}\bra{j} \otimes e ^ {i P \ theta_j}.</span><span class="sxs-lookup"><span data-stu-id="5b8da-109">$$ \begin{align} U = \sum^{2^n - 1}_{j=0} \ket{j}\bra{j} \otimes e^{i P \theta_j}.</span></span>
<span data-ttu-id="5b8da-110">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="5b8da-110">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="5b8da-111">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5b8da-111">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="5b8da-112">Koeffizienten: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="5b8da-112">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="5b8da-113">Array von bis zu $2 ^ n $ Koeffizienten $ \ theta_j $.</span><span class="sxs-lookup"><span data-stu-id="5b8da-113">Array of up to $2^n$ coefficients $\theta_j$.</span></span> <span data-ttu-id="5b8da-114">Der $j $ Th-Koeffizienten indiziert den im Little-Endian-Format codierten Zahlen Status $ \ket{j} $.</span><span class="sxs-lookup"><span data-stu-id="5b8da-114">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="pauli--pauli"></a><span data-ttu-id="5b8da-115">Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="5b8da-115">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="5b8da-116">Der Pauli-Operator $P $, der die Achse der Drehung bestimmt.</span><span class="sxs-lookup"><span data-stu-id="5b8da-116">Pauli operator $P$ that determines axis of rotation.</span></span>


### <a name="control--littleendian"></a><span data-ttu-id="5b8da-117">Control: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="5b8da-117">control : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="5b8da-118">$n $-Qubit-Steuerelement Register, das die Anzahl der Zustände $ \ket{j} $ im Little-Endian-Format codiert.</span><span class="sxs-lookup"><span data-stu-id="5b8da-118">$n$-qubit control register that encodes number states $\ket{j}$ in little-endian format.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="5b8da-119">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="5b8da-119">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="5b8da-120">Einzelnes Qubit-Register, das durch $e ^ {i P \ theta_j} $ gedreht wird.</span><span class="sxs-lookup"><span data-stu-id="5b8da-120">Single qubit register that is rotated by $e^{i P \theta_j}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5b8da-121">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5b8da-121">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="5b8da-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5b8da-122">Remarks</span></span>

<span data-ttu-id="5b8da-123">`coefficients` wird mit Elementen $ \ theta_j = $0,0 aufgefüllt, wenn weniger als $2 ^ n $ angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5b8da-123">`coefficients` will be padded with elements $\theta_j = 0.0$ if fewer than $2^n$ are specified.</span></span>

## <a name="see-also"></a><span data-ttu-id="5b8da-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5b8da-124">See Also</span></span>

- [<span data-ttu-id="5b8da-125">Microsoft. Quantum. Canon. näherymultiplexpauli</span><span class="sxs-lookup"><span data-stu-id="5b8da-125">Microsoft.Quantum.Canon.ApproximatelyMultiplexPauli</span></span>](xref:Microsoft.Quantum.Canon.ApproximatelyMultiplexPauli)
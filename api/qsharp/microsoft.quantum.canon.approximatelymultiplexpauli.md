---
uid: Microsoft.Quantum.Canon.ApproximatelyMultiplexPauli
title: Ungefäatelymultiplexpauli-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApproximatelyMultiplexPauli
qsharp.summary: Applies a Pauli rotation conditioned on an array of qubits, truncating small rotation angles according to a given tolerance.
ms.openlocfilehash: c91937d9e82a2a1514d81529adb35a5f804a0e13
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704538"
---
# <a name="approximatelymultiplexpauli-operation"></a><span data-ttu-id="f0cb1-102">Ungefäatelymultiplexpauli-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f0cb1-102">ApproximatelyMultiplexPauli operation</span></span>

<span data-ttu-id="f0cb1-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f0cb1-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f0cb1-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f0cb1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f0cb1-105">Wendet eine für ein Array von Qubits bedingte Pauli-Drehung an und verkürzt kleine Drehwinkel entsprechend einer gegebenen Toleranz.</span><span class="sxs-lookup"><span data-stu-id="f0cb1-105">Applies a Pauli rotation conditioned on an array of qubits, truncating small rotation angles according to a given tolerance.</span></span>

```qsharp
operation ApproximatelyMultiplexPauli (tolerance : Double, coefficients : Double[], pauli : Pauli, control : Microsoft.Quantum.Arithmetic.LittleEndian, target : Qubit) : Unit
```


## <a name="description"></a><span data-ttu-id="f0cb1-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f0cb1-106">Description</span></span>

<span data-ttu-id="f0cb1-107">Dadurch wird ein mehrfach gesteuerter einheitlicher Vorgang angewendet, bei dem die Drehung um den Winkel $ \ theta_j $ um einen Single-Qubit-Pauli-Operator $P $ durchführt, wenn er vom $n $-Qubit-Zahlen Status $ \ket{j} $ gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="f0cb1-107">This applies a multiply controlled unitary operation that performs rotations by angle $\theta_j$ about single-qubit Pauli operator $P$ when controlled by the $n$-qubit number state $\ket{j}$.</span></span>
<span data-ttu-id="f0cb1-108">Insbesondere wird die Aktion dieses Vorgangs durch die einheitliche</span><span class="sxs-lookup"><span data-stu-id="f0cb1-108">In particular, the action of this operation is represented by the unitary</span></span>

<span data-ttu-id="f0cb1-109">$ $ \begin{align} U = \sum ^ {2 ^ n-1} _ {j = 0} \ket{j}\bra{j} \otimes e ^ {i P \ theta_j}.</span><span class="sxs-lookup"><span data-stu-id="f0cb1-109">$$ \begin{align} U = \sum^{2^n - 1}_{j=0} \ket{j}\bra{j} \otimes e^{i P \theta_j}.</span></span>
<span data-ttu-id="f0cb1-110">\end{align}</span><span class="sxs-lookup"><span data-stu-id="f0cb1-110">\end{align}</span></span>

##

## <a name="input"></a><span data-ttu-id="f0cb1-111">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f0cb1-111">Input</span></span>

### <a name="tolerance--double"></a><span data-ttu-id="f0cb1-112">Toleranz: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="f0cb1-112">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="f0cb1-113">Eine Toleranz, unter der kleine Koeffizienten abgeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="f0cb1-113">A tolerance below which small coefficients are truncated.</span></span>


### <a name="coefficients--double"></a><span data-ttu-id="f0cb1-114">Koeffizienten: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="f0cb1-114">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="f0cb1-115">Array von bis zu $2 ^ n $ Koeffizienten $ \ theta_j $.</span><span class="sxs-lookup"><span data-stu-id="f0cb1-115">Array of up to $2^n$ coefficients $\theta_j$.</span></span> <span data-ttu-id="f0cb1-116">Der $j $ Th-Koeffizienten indiziert den im Little-Endian-Format codierten Zahlen Status $ \ket{j} $.</span><span class="sxs-lookup"><span data-stu-id="f0cb1-116">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="pauli--pauli"></a><span data-ttu-id="f0cb1-117">Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="f0cb1-117">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="f0cb1-118">Der Pauli-Operator $P $, der die Achse der Drehung bestimmt.</span><span class="sxs-lookup"><span data-stu-id="f0cb1-118">Pauli operator $P$ that determines axis of rotation.</span></span>


### <a name="control--littleendian"></a><span data-ttu-id="f0cb1-119">Control: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="f0cb1-119">control : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="f0cb1-120">$n $-Qubit-Steuerelement Register, das die Anzahl der Zustände $ \ket{j} $ im Little-Endian-Format codiert.</span><span class="sxs-lookup"><span data-stu-id="f0cb1-120">$n$-qubit control register that encodes number states $\ket{j}$ in little-endian format.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="f0cb1-121">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="f0cb1-121">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="f0cb1-122">Einzelnes Qubit-Register, das durch $e ^ {i P \ theta_j} $ gedreht wird.</span><span class="sxs-lookup"><span data-stu-id="f0cb1-122">Single qubit register that is rotated by $e^{i P \theta_j}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f0cb1-123">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f0cb1-123">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="f0cb1-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f0cb1-124">Remarks</span></span>

<span data-ttu-id="f0cb1-125">`coefficients` wird mit Elementen $ \ theta_j = $0,0 aufgefüllt, wenn weniger als $2 ^ n $ angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f0cb1-125">`coefficients` will be padded with elements $\theta_j = 0.0$ if fewer than $2^n$ are specified.</span></span>

## <a name="see-also"></a><span data-ttu-id="f0cb1-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f0cb1-126">See Also</span></span>

- [<span data-ttu-id="f0cb1-127">Microsoft. Quantum. Canon. multiplexpauli</span><span class="sxs-lookup"><span data-stu-id="f0cb1-127">Microsoft.Quantum.Canon.MultiplexPauli</span></span>](xref:Microsoft.Quantum.Canon.MultiplexPauli)
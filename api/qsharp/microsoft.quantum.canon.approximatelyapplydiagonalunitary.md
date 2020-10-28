---
uid: Microsoft.Quantum.Canon.ApproximatelyApplyDiagonalUnitary
title: Ungefäatelyapplydiagonaleinheitlicher-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApproximatelyApplyDiagonalUnitary
qsharp.summary: Applies an array of complex phases to numeric basis states of a register of qubits, truncating small rotation angles according to a given tolerance.
ms.openlocfilehash: 9d9b1ced320b142aef2a2cd8f3335f855d37048f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704543"
---
# <a name="approximatelyapplydiagonalunitary-operation"></a><span data-ttu-id="b934d-102">Ungefäatelyapplydiagonaleinheitlicher-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b934d-102">ApproximatelyApplyDiagonalUnitary operation</span></span>

<span data-ttu-id="b934d-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="b934d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="b934d-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b934d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b934d-105">Wendet ein Array komplexer Phasen auf numerische Basiszustände eines Register von Qubits an und verkürzt kleine Drehwinkel entsprechend einer bestimmten Toleranz.</span><span class="sxs-lookup"><span data-stu-id="b934d-105">Applies an array of complex phases to numeric basis states of a register of qubits, truncating small rotation angles according to a given tolerance.</span></span>

```qsharp
operation ApproximatelyApplyDiagonalUnitary (tolerance : Double, coefficients : Double[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="b934d-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b934d-106">Description</span></span>

<span data-ttu-id="b934d-107">Mit diesem Vorgang wird eine Diagonale einheitliche implementiert, die eine komplexe Phase $e ^ {i \ theta_j} $ auf dem $n $-Qubit-Zahlen Status $ \ket{j} $ anwendet.</span><span class="sxs-lookup"><span data-stu-id="b934d-107">This operation implements a diagonal unitary that applies a complex phase $e^{i \theta_j}$ on the $n$-qubit number state $\ket{j}$.</span></span>
<span data-ttu-id="b934d-108">Insbesondere kann dieser Vorgang durch die einheitliche</span><span class="sxs-lookup"><span data-stu-id="b934d-108">In particular, this operation can be represented by the unitary</span></span>

<span data-ttu-id="b934d-109">$ $ \begin{align} U = \sum ^ {2 ^ n-1} _ {j = 0} e ^ {i \ theta_j} \ket{j}\bra{j}.</span><span class="sxs-lookup"><span data-stu-id="b934d-109">$$ \begin{align} U = \sum^{2^n-1}_{j=0}e^{i\theta_j}\ket{j}\bra{j}.</span></span>
<span data-ttu-id="b934d-110">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="b934d-110">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="b934d-111">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b934d-111">Input</span></span>

### <a name="tolerance--double"></a><span data-ttu-id="b934d-112">Toleranz: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="b934d-112">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="b934d-113">Eine Toleranz, unter der kleine Koeffizienten abgeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="b934d-113">A tolerance below which small coefficients are truncated.</span></span>


### <a name="coefficients--double"></a><span data-ttu-id="b934d-114">Koeffizienten: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="b934d-114">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="b934d-115">Array von bis zu $2 ^ n $ Koeffizienten $ \ theta_j $.</span><span class="sxs-lookup"><span data-stu-id="b934d-115">Array of up to $2^n$ coefficients $\theta_j$.</span></span> <span data-ttu-id="b934d-116">Der $j $ Th-Koeffizienten indiziert den im Little-Endian-Format codierten Zahlen Status $ \ket{j} $.</span><span class="sxs-lookup"><span data-stu-id="b934d-116">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="b934d-117">Qubits: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="b934d-117">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="b934d-118">$n $-Qubit-Steuerelement Register, das die Anzahl der Zustände $ \ket{j} $ im Little-Endian-Format codiert.</span><span class="sxs-lookup"><span data-stu-id="b934d-118">$n$-qubit control register that encodes number states $\ket{j}$ in little-endian format.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b934d-119">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b934d-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="b934d-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b934d-120">Remarks</span></span>

<span data-ttu-id="b934d-121">`coefficients` wird mit Elementen $ \ theta_j = $0,0 aufgefüllt, wenn weniger als $2 ^ n $ angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b934d-121">`coefficients` will be padded with elements $\theta_j = 0.0$ if fewer than $2^n$ are specified.</span></span>

## <a name="references"></a><span data-ttu-id="b934d-122">Referenzen</span><span class="sxs-lookup"><span data-stu-id="b934d-122">References</span></span>

- <span data-ttu-id="b934d-123">Synthese von Quantum Logic-Leitungen Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span><span class="sxs-lookup"><span data-stu-id="b934d-123">Synthesis of Quantum Logic Circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span></span>

## <a name="see-also"></a><span data-ttu-id="b934d-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b934d-124">See Also</span></span>

- [<span data-ttu-id="b934d-125">Microsoft. Quantum. Canon. applydiagonaleinheitlicher</span><span class="sxs-lookup"><span data-stu-id="b934d-125">Microsoft.Quantum.Canon.ApplyDiagonalUnitary</span></span>](xref:Microsoft.Quantum.Canon.ApplyDiagonalUnitary)
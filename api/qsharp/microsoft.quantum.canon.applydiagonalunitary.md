---
uid: Microsoft.Quantum.Canon.ApplyDiagonalUnitary
title: Applydiagonaleinheitlicher-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyDiagonalUnitary
qsharp.summary: Applies an array of complex phases to numeric basis states of a register of qubits.
ms.openlocfilehash: 14ab8d7beddda26594967225934d472d52bac9eb
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841886"
---
# <a name="applydiagonalunitary-operation"></a><span data-ttu-id="a0b0d-102">Applydiagonaleinheitlicher-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a0b0d-102">ApplyDiagonalUnitary operation</span></span>

<span data-ttu-id="a0b0d-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a0b0d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a0b0d-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a0b0d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a0b0d-105">Wendet ein Array komplexer Phasen auf numerische Basiszustände eines Register von Qubits an.</span><span class="sxs-lookup"><span data-stu-id="a0b0d-105">Applies an array of complex phases to numeric basis states of a register of qubits.</span></span>

```qsharp
operation ApplyDiagonalUnitary (coefficients : Double[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="a0b0d-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a0b0d-106">Description</span></span>

<span data-ttu-id="a0b0d-107">Mit diesem Vorgang wird eine Diagonale einheitliche implementiert, die eine komplexe Phase $e ^ {i \ theta_j} $ auf dem $n $-Qubit-Zahlen Status $ \ket{j} $ anwendet.</span><span class="sxs-lookup"><span data-stu-id="a0b0d-107">This operation implements a diagonal unitary that applies a complex phase $e^{i \theta_j}$ on the $n$-qubit number state $\ket{j}$.</span></span>
<span data-ttu-id="a0b0d-108">Insbesondere kann dieser Vorgang durch die einheitliche</span><span class="sxs-lookup"><span data-stu-id="a0b0d-108">In particular, this operation can be represented by the unitary</span></span>

<span data-ttu-id="a0b0d-109">$ $ \begin{align} U = \sum ^ {2 ^ n-1} _ {j = 0} e ^ {i \ theta_j} \ket{j}\bra{j}.</span><span class="sxs-lookup"><span data-stu-id="a0b0d-109">$$ \begin{align} U = \sum^{2^n-1}_{j=0}e^{i\theta_j}\ket{j}\bra{j}.</span></span>
<span data-ttu-id="a0b0d-110">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="a0b0d-110">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="a0b0d-111">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a0b0d-111">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="a0b0d-112">Koeffizienten: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="a0b0d-112">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="a0b0d-113">Array von bis zu $2 ^ n $ Koeffizienten $ \ theta_j $.</span><span class="sxs-lookup"><span data-stu-id="a0b0d-113">Array of up to $2^n$ coefficients $\theta_j$.</span></span> <span data-ttu-id="a0b0d-114">Der $j $ Th-Koeffizienten indiziert den im Little-Endian-Format codierten Zahlen Status $ \ket{j} $.</span><span class="sxs-lookup"><span data-stu-id="a0b0d-114">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="a0b0d-115">Qubits: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="a0b0d-115">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="a0b0d-116">$n $-Qubit-Steuerelement Register, das die Anzahl der Zustände $ \ket{j} $ im Little-Endian-Format codiert.</span><span class="sxs-lookup"><span data-stu-id="a0b0d-116">$n$-qubit control register that encodes number states $\ket{j}$ in little-endian format.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a0b0d-117">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a0b0d-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="a0b0d-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a0b0d-118">Remarks</span></span>

<span data-ttu-id="a0b0d-119">`coefficients` wird mit Elementen $ \ theta_j = $0,0 aufgefüllt, wenn weniger als $2 ^ n $ angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a0b0d-119">`coefficients` will be padded with elements $\theta_j = 0.0$ if fewer than $2^n$ are specified.</span></span>

## <a name="references"></a><span data-ttu-id="a0b0d-120">References</span><span class="sxs-lookup"><span data-stu-id="a0b0d-120">References</span></span>

- <span data-ttu-id="a0b0d-121">Synthese von Quantum Logic-Leitungen Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span><span class="sxs-lookup"><span data-stu-id="a0b0d-121">Synthesis of Quantum Logic Circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span></span>

## <a name="see-also"></a><span data-ttu-id="a0b0d-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a0b0d-122">See Also</span></span>

- [<span data-ttu-id="a0b0d-123">Microsoft. Quantum. Canon. ungefähre atelyapplydiagonaleinheitlicher</span><span class="sxs-lookup"><span data-stu-id="a0b0d-123">Microsoft.Quantum.Canon.ApproximatelyApplyDiagonalUnitary</span></span>](xref:Microsoft.Quantum.Canon.ApproximatelyApplyDiagonalUnitary)
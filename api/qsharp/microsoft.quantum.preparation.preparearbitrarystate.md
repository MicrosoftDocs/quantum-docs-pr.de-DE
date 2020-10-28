---
uid: Microsoft.Quantum.Preparation.PrepareArbitraryState
title: Preparearbitrarystate-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareArbitraryState
qsharp.summary: Given a set of coefficients and a little-endian encoded quantum register, prepares an state on that register described by the given coefficients.
ms.openlocfilehash: 18f45da601b02fc5f83936b086323e31a66fc20b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724040"
---
# <a name="preparearbitrarystate-operation"></a><span data-ttu-id="7fd72-102">Preparearbitrarystate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7fd72-102">PrepareArbitraryState operation</span></span>

<span data-ttu-id="7fd72-103">Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="7fd72-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="7fd72-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7fd72-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7fd72-105">Bereitet einen Satz von Koeffizienten und ein Little-Endian-codiertes Quantum-Register vor und bereitet einen Status für dieses Register vor, der von den gegebenen Koeffizienten beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="7fd72-105">Given a set of coefficients and a little-endian encoded quantum register, prepares an state on that register described by the given coefficients.</span></span>

```qsharp
operation PrepareArbitraryState (coefficients : Microsoft.Quantum.Math.ComplexPolar[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="7fd72-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7fd72-106">Description</span></span>

<span data-ttu-id="7fd72-107">Mit diesem Vorgang wird ein beliebiger Quantum-Status "$ \ket{\psi} $" mit komplexen Koeffizienten $r _J e ^ {i t_j} $ aus dem $n $-Qubit-Berechnungsbasis Status $ \ket{0\cdots 0} $ vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="7fd72-107">This operation prepares an arbitrary quantum state $\ket{\psi}$ with complex coefficients $r_j e^{i t_j}$ from the $n$-qubit computational basis state $\ket{0 \cdots 0}$.</span></span>
<span data-ttu-id="7fd72-108">Insbesondere kann die Aktion dieses Vorgangs durch eine einheitliche Transformation $U $ simuliert werden, die den Zustand "alle Nullen" als</span><span class="sxs-lookup"><span data-stu-id="7fd72-108">In particular, the action of this operation can be simulated by the a unitary transformation $U$ which acts on the all-zeros state as</span></span>

<span data-ttu-id="7fd72-109">$ $ \begin{align} u\ket {0... 0} & = \ket{\psi} \\ \\ & = \bruchteil {\ sum_ {j = 0} ^ {2 ^ n-1} r_j e ^ {i t_j} \ket{j}} {\sqrt{\ sum_ {j = 0} ^ {2 ^ n-1} | r_j | ^ 2}}.</span><span class="sxs-lookup"><span data-stu-id="7fd72-109">$$ \begin{align} U\ket{0...0} & = \ket{\psi} \\\\ & = \frac{ \sum_{j=0}^{2^n-1} r_j e^{i t_j} \ket{j} }{ \sqrt{\sum_{j=0}^{2^n-1} |r_j|^2} }.</span></span>
<span data-ttu-id="7fd72-110">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="7fd72-110">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="7fd72-111">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7fd72-111">Input</span></span>

### <a name="coefficients--complexpolar"></a><span data-ttu-id="7fd72-112">Koeffizienten: [complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)[]</span><span class="sxs-lookup"><span data-stu-id="7fd72-112">coefficients : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)[]</span></span>

<span data-ttu-id="7fd72-113">Array von bis zu $2 ^ n $ komplexen Koeffizienten, die durch ihren absoluten Wert und Phase $ (r_j, t_j) $ dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="7fd72-113">Array of up to $2^n$ complex coefficients represented by their absolute value and phase $(r_j, t_j)$.</span></span> <span data-ttu-id="7fd72-114">Der $j $ Th-Koeffizienten indiziert den im Little-Endian-Format codierten Zahlen Status $ \ket{j} $.</span><span class="sxs-lookup"><span data-stu-id="7fd72-114">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="7fd72-115">Qubits: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="7fd72-115">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="7fd72-116">Der Qubit-Registrierungsstatus wird im Little-Endian-Format registriert.</span><span class="sxs-lookup"><span data-stu-id="7fd72-116">Qubit register encoding number states in little-endian format.</span></span> <span data-ttu-id="7fd72-117">Diese Initialisierung wird im Berechnungsbasis Status $ \ket{0...0} $ erwartet.</span><span class="sxs-lookup"><span data-stu-id="7fd72-117">This is expected to be initialized in the computational basis state $\ket{0...0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7fd72-118">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7fd72-118">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="7fd72-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7fd72-119">Remarks</span></span>

<span data-ttu-id="7fd72-120">Negative Eingabe Koeffizienten $r _J < $0 werden als positiv mit dem Wert $ | r_j | $ behandelt.</span><span class="sxs-lookup"><span data-stu-id="7fd72-120">Negative input coefficients $r_j < 0$ will be treated as though positive with value $|r_j|$.</span></span> <span data-ttu-id="7fd72-121">`coefficients` wird mit den Elementen $ (r_j, t_j) = (0,0, 0,0) $ aufgefüllt, wenn weniger als $2 ^ n $ angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7fd72-121">`coefficients` will be padded with elements $(r_j, t_j) = (0.0, 0.0)$ if fewer than $2^n$ are specified.</span></span>

## <a name="references"></a><span data-ttu-id="7fd72-122">Referenzen</span><span class="sxs-lookup"><span data-stu-id="7fd72-122">References</span></span>

- <span data-ttu-id="7fd72-123">Synthese von Quantum Logic-Leitungen Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span><span class="sxs-lookup"><span data-stu-id="7fd72-123">Synthesis of Quantum Logic Circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span></span>

## <a name="see-also"></a><span data-ttu-id="7fd72-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7fd72-124">See Also</span></span>

- [<span data-ttu-id="7fd72-125">Microsoft. Quantum. Preparation. ungefähre atelypreparearbitrarystate</span><span class="sxs-lookup"><span data-stu-id="7fd72-125">Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryState</span></span>](xref:Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryState)
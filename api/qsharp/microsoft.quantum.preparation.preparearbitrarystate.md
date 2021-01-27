---
uid: Microsoft.Quantum.Preparation.PrepareArbitraryState
title: Preparearbitrarystate-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareArbitraryState
qsharp.summary: >-
  > [!WARNING]

  > PrepareArbitraryState has been deprecated. Please use <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateCP> instead.


  Given a set of coefficients and a little-endian encoded quantum register, prepares an state on that register described by the given coefficients.
ms.openlocfilehash: e2e4818e5d30b17dd1984c36da92d76b84403e1c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842383"
---
# <a name="preparearbitrarystate-operation"></a><span data-ttu-id="90a15-102">Preparearbitrarystate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="90a15-102">PrepareArbitraryState operation</span></span>

<span data-ttu-id="90a15-103">Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="90a15-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="90a15-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="90a15-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="90a15-105">Preparearbitrarystate wurde als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="90a15-105">PrepareArbitraryState has been deprecated.</span></span> <span data-ttu-id="90a15-106">Verwenden Sie stattdessen <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateCP>.</span><span class="sxs-lookup"><span data-stu-id="90a15-106">Please use <xref:Microsoft.Quantum.Preparation.PrepareArbitraryStateCP> instead.</span></span>

<span data-ttu-id="90a15-107">Bereitet einen Satz von Koeffizienten und ein Little-Endian-codiertes Quantum-Register vor und bereitet einen Status für dieses Register vor, der von den gegebenen Koeffizienten beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="90a15-107">Given a set of coefficients and a little-endian encoded quantum register, prepares an state on that register described by the given coefficients.</span></span>

```qsharp
operation PrepareArbitraryState (coefficients : Microsoft.Quantum.Math.ComplexPolar[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="90a15-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="90a15-108">Description</span></span>

<span data-ttu-id="90a15-109">Mit diesem Vorgang wird ein beliebiger Quantum-Status "$ \ket{\psi} $" mit komplexen Koeffizienten $r _J e ^ {i t_j} $ aus dem $n $-Qubit-Berechnungsbasis Status $ \ket{0\cdots 0} $ vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="90a15-109">This operation prepares an arbitrary quantum state $\ket{\psi}$ with complex coefficients $r_j e^{i t_j}$ from the $n$-qubit computational basis state $\ket{0 \cdots 0}$.</span></span>
<span data-ttu-id="90a15-110">Insbesondere kann die Aktion dieses Vorgangs durch eine einheitliche Transformation $U $ simuliert werden, die den Zustand "alle Nullen" als</span><span class="sxs-lookup"><span data-stu-id="90a15-110">In particular, the action of this operation can be simulated by the a unitary transformation $U$ which acts on the all-zeros state as</span></span>

<span data-ttu-id="90a15-111">$ $ \begin{align} u\ket {0... 0} & = \ket{\psi} \\ \\ & = \bruchteil {\ sum_ {j = 0} ^ {2 ^ n-1} r_j e ^ {i t_j} \ket{j}} {\sqrt{\ sum_ {j = 0} ^ {2 ^ n-1} | r_j | ^ 2}}.</span><span class="sxs-lookup"><span data-stu-id="90a15-111">$$ \begin{align} U\ket{0...0} & = \ket{\psi} \\\\ & = \frac{ \sum_{j=0}^{2^n-1} r_j e^{i t_j} \ket{j} }{ \sqrt{\sum_{j=0}^{2^n-1} |r_j|^2} }.</span></span>
<span data-ttu-id="90a15-112">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="90a15-112">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="90a15-113">Eingabe</span><span class="sxs-lookup"><span data-stu-id="90a15-113">Input</span></span>

### <a name="coefficients--complexpolar"></a><span data-ttu-id="90a15-114">Koeffizienten: [complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)[]</span><span class="sxs-lookup"><span data-stu-id="90a15-114">coefficients : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)[]</span></span>

<span data-ttu-id="90a15-115">Array von bis zu $2 ^ n $ komplexen Koeffizienten, die durch ihren absoluten Wert und Phase $ (r_j, t_j) $ dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="90a15-115">Array of up to $2^n$ complex coefficients represented by their absolute value and phase $(r_j, t_j)$.</span></span> <span data-ttu-id="90a15-116">Der $j $ Th-Koeffizienten indiziert den im Little-Endian-Format codierten Zahlen Status $ \ket{j} $.</span><span class="sxs-lookup"><span data-stu-id="90a15-116">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="90a15-117">Qubits: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="90a15-117">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="90a15-118">Der Qubit-Registrierungsstatus wird im Little-Endian-Format registriert.</span><span class="sxs-lookup"><span data-stu-id="90a15-118">Qubit register encoding number states in little-endian format.</span></span> <span data-ttu-id="90a15-119">Diese Initialisierung wird im Berechnungsbasis Status $ \ket{0...0} $ erwartet.</span><span class="sxs-lookup"><span data-stu-id="90a15-119">This is expected to be initialized in the computational basis state $\ket{0...0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="90a15-120">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="90a15-120">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="90a15-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="90a15-121">Remarks</span></span>

<span data-ttu-id="90a15-122">Negative Eingabe Koeffizienten $r _J < $0 werden als positiv mit dem Wert $ | r_j | $ behandelt.</span><span class="sxs-lookup"><span data-stu-id="90a15-122">Negative input coefficients $r_j < 0$ will be treated as though positive with value $|r_j|$.</span></span> <span data-ttu-id="90a15-123">`coefficients` wird mit den Elementen $ (r_j, t_j) = (0,0, 0,0) $ aufgefüllt, wenn weniger als $2 ^ n $ angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="90a15-123">`coefficients` will be padded with elements $(r_j, t_j) = (0.0, 0.0)$ if fewer than $2^n$ are specified.</span></span>

## <a name="references"></a><span data-ttu-id="90a15-124">References</span><span class="sxs-lookup"><span data-stu-id="90a15-124">References</span></span>

- <span data-ttu-id="90a15-125">Synthese von Quantum Logic-Leitungen Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span><span class="sxs-lookup"><span data-stu-id="90a15-125">Synthesis of Quantum Logic Circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span></span>

## <a name="see-also"></a><span data-ttu-id="90a15-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="90a15-126">See Also</span></span>

- [<span data-ttu-id="90a15-127">Microsoft. Quantum. Preparation. ungefähre atelypreparearbitrarystate</span><span class="sxs-lookup"><span data-stu-id="90a15-127">Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryState</span></span>](xref:Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryState)
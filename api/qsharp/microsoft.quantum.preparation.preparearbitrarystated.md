---
uid: Microsoft.Quantum.Preparation.PrepareArbitraryStateD
title: Preparearbitraryat-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareArbitraryStateD
qsharp.summary: Given a set of coefficients and a little-endian encoded quantum register, prepares an state on that register described by the given coefficients.
ms.openlocfilehash: 61f6614821951435828cd28edeb1447cb33f3648
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842374"
---
# <a name="preparearbitrarystated-operation"></a><span data-ttu-id="c4cc2-102">Preparearbitraryat-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c4cc2-102">PrepareArbitraryStateD operation</span></span>

<span data-ttu-id="c4cc2-103">Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="c4cc2-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="c4cc2-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c4cc2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c4cc2-105">Bereitet einen Satz von Koeffizienten und ein Little-Endian-codiertes Quantum-Register vor und bereitet einen Status für dieses Register vor, der von den gegebenen Koeffizienten beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="c4cc2-105">Given a set of coefficients and a little-endian encoded quantum register, prepares an state on that register described by the given coefficients.</span></span>

```qsharp
operation PrepareArbitraryStateD (coefficients : Double[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="c4cc2-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4cc2-106">Description</span></span>

<span data-ttu-id="c4cc2-107">Mit diesem Vorgang wird ein beliebiger Quantum-Status "$ \ket{\psi} $" mit komplexen Koeffizienten $r _J e ^ {i t_j} $ aus dem $n $-Qubit-Berechnungsbasis Status $ \ket{0\cdots 0} $ vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="c4cc2-107">This operation prepares an arbitrary quantum state $\ket{\psi}$ with complex coefficients $r_j e^{i t_j}$ from the $n$-qubit computational basis state $\ket{0 \cdots 0}$.</span></span>
<span data-ttu-id="c4cc2-108">Insbesondere kann die Aktion dieses Vorgangs durch eine einheitliche Transformation $U $ simuliert werden, die den Zustand "alle Nullen" als</span><span class="sxs-lookup"><span data-stu-id="c4cc2-108">In particular, the action of this operation can be simulated by the a unitary transformation $U$ that acts on the all-zeros state as</span></span>

<span data-ttu-id="c4cc2-109">$ $ \begin{align} u\ket {0... 0} & = \ket{\psi} \\ \\ & = \bruchteil {\ sum_ {j = 0} ^ {2 ^ n-1} r_j e ^ {i t_j} \ket{j}} {\sqrt{\ sum_ {j = 0} ^ {2 ^ n-1} | r_j | ^ 2}}.</span><span class="sxs-lookup"><span data-stu-id="c4cc2-109">$$ \begin{align} U\ket{0...0} & = \ket{\psi} \\\\ & = \frac{ \sum_{j=0}^{2^n-1} r_j e^{i t_j} \ket{j} }{ \sqrt{\sum_{j=0}^{2^n-1} |r_j|^2} }.</span></span>
<span data-ttu-id="c4cc2-110">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="c4cc2-110">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="c4cc2-111">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c4cc2-111">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="c4cc2-112">Koeffizienten: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="c4cc2-112">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="c4cc2-113">Array von bis zu $2 ^ n $ Real Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="c4cc2-113">Array of up to $2^n$ real coefficients.</span></span> <span data-ttu-id="c4cc2-114">Der $j $ Th-Koeffizienten indiziert den im Little-Endian-Format codierten Zahlen Status $ \ket{j} $.</span><span class="sxs-lookup"><span data-stu-id="c4cc2-114">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="c4cc2-115">Qubits: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="c4cc2-115">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="c4cc2-116">Der Qubit-Registrierungsstatus wird im Little-Endian-Format registriert.</span><span class="sxs-lookup"><span data-stu-id="c4cc2-116">Qubit register encoding number states in little-endian format.</span></span> <span data-ttu-id="c4cc2-117">Diese Initialisierung wird im Berechnungsbasis Status $ \ket{0...0} $ erwartet.</span><span class="sxs-lookup"><span data-stu-id="c4cc2-117">This is expected to be initialized in the computational basis state $\ket{0...0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c4cc2-118">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c4cc2-118">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="c4cc2-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c4cc2-119">Remarks</span></span>

<span data-ttu-id="c4cc2-120">Negative Eingabe Koeffizienten $r _J < $0 werden als positiv mit dem Wert $ | r_j | $ behandelt.</span><span class="sxs-lookup"><span data-stu-id="c4cc2-120">Negative input coefficients $r_j < 0$ will be treated as though positive with value $|r_j|$.</span></span> <span data-ttu-id="c4cc2-121">`coefficients` wird mit den Elementen $ (r_j, t_j) = (0,0, 0,0) $ aufgefüllt, wenn weniger als $2 ^ n $ angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c4cc2-121">`coefficients` will be padded with elements $(r_j, t_j) = (0.0, 0.0)$ if fewer than $2^n$ are specified.</span></span>

## <a name="references"></a><span data-ttu-id="c4cc2-122">References</span><span class="sxs-lookup"><span data-stu-id="c4cc2-122">References</span></span>

- <span data-ttu-id="c4cc2-123">Synthese von Quantum Logic-Leitungen Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span><span class="sxs-lookup"><span data-stu-id="c4cc2-123">Synthesis of Quantum Logic Circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span></span>

## <a name="see-also"></a><span data-ttu-id="c4cc2-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c4cc2-124">See Also</span></span>

- [<span data-ttu-id="c4cc2-125">Microsoft. Quantum. Preparation. ungefähre atelypreparearbitrarystate</span><span class="sxs-lookup"><span data-stu-id="c4cc2-125">Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryState</span></span>](xref:Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryState)
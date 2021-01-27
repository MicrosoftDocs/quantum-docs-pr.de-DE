---
uid: Microsoft.Quantum.Preparation.ApproximatelyPrepareArbitraryStateCP
title: Ungefäatelypreparearbitrarystatus ECP-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: ApproximatelyPrepareArbitraryStateCP
qsharp.summary: Given a set of coefficients and a little-endian encoded quantum register, prepares an state on that register described by the given coefficients, up to a given approximation tolerance.
ms.openlocfilehash: fbabc320ff153dbceb4453bad95cd5f4c1776583
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856971"
---
# <a name="approximatelypreparearbitrarystatecp-operation"></a><span data-ttu-id="1d589-102">Ungefäatelypreparearbitrarystatus ECP-Vorgang</span><span class="sxs-lookup"><span data-stu-id="1d589-102">ApproximatelyPrepareArbitraryStateCP operation</span></span>

<span data-ttu-id="1d589-103">Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="1d589-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="1d589-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1d589-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1d589-105">Bereitet mithilfe eines Satzes von Koeffizienten und einem Little-Endian-codierten Quantum-Register einen Zustand für dieses Register vor, der durch die angegebenen Koeffizienten beschrieben wird, bis zu einer bestimmten Näherungs Toleranz.</span><span class="sxs-lookup"><span data-stu-id="1d589-105">Given a set of coefficients and a little-endian encoded quantum register, prepares an state on that register described by the given coefficients, up to a given approximation tolerance.</span></span>

```qsharp
operation ApproximatelyPrepareArbitraryStateCP (tolerance : Double, coefficients : Microsoft.Quantum.Math.ComplexPolar[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="1d589-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1d589-106">Description</span></span>

<span data-ttu-id="1d589-107">Mit diesem Vorgang wird ein beliebiger Quantum-Status "$ \ket{\psi} $" mit komplexen Koeffizienten $r _J e ^ {i t_j} $ aus dem $n $-Qubit-Berechnungsbasis Status $ \ket{0\cdots 0} $ vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="1d589-107">This operation prepares an arbitrary quantum state $\ket{\psi}$ with complex coefficients $r_j e^{i t_j}$ from the $n$-qubit computational basis state $\ket{0 \cdots 0}$.</span></span>
<span data-ttu-id="1d589-108">Insbesondere kann die Aktion dieses Vorgangs durch eine einheitliche Transformation $U $ simuliert werden, die den Zustand "alle Nullen" als</span><span class="sxs-lookup"><span data-stu-id="1d589-108">In particular, the action of this operation can be simulated by the a unitary transformation $U$ which acts on the all-zeros state as</span></span>

<span data-ttu-id="1d589-109">$ $ \begin{align} u\ket {0... 0} & = \ket{\psi} \\ \\ & = \bruchteil {\ sum_ {j = 0} ^ {2 ^ n-1} r_j e ^ {i t_j} \ket{j}} {\sqrt{\ sum_ {j = 0} ^ {2 ^ n-1} | r_j | ^ 2}}.</span><span class="sxs-lookup"><span data-stu-id="1d589-109">$$ \begin{align} U\ket{0...0} & = \ket{\psi} \\\\ & = \frac{ \sum_{j=0}^{2^n-1} r_j e^{i t_j} \ket{j} }{ \sqrt{\sum_{j=0}^{2^n-1} |r_j|^2} }.</span></span>
<span data-ttu-id="1d589-110">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="1d589-110">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="1d589-111">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1d589-111">Input</span></span>

### <a name="tolerance--double"></a><span data-ttu-id="1d589-112">Toleranz: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="1d589-112">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="1d589-113">Die Näherungs Toleranz, die beim Vorbereiten des angegebenen Zustands verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1d589-113">The approximation tolerance to be used when preparing the given state.</span></span>


### <a name="coefficients--complexpolar"></a><span data-ttu-id="1d589-114">Koeffizienten: [complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)[]</span><span class="sxs-lookup"><span data-stu-id="1d589-114">coefficients : [ComplexPolar](xref:Microsoft.Quantum.Math.ComplexPolar)[]</span></span>

<span data-ttu-id="1d589-115">Array von bis zu $2 ^ n $ komplexen Koeffizienten, die durch ihren absoluten Wert und Phase $ (r_j, t_j) $ dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="1d589-115">Array of up to $2^n$ complex coefficients represented by their absolute value and phase $(r_j, t_j)$.</span></span> <span data-ttu-id="1d589-116">Der $j $ Th-Koeffizienten indiziert den im Little-Endian-Format codierten Zahlen Status $ \ket{j} $.</span><span class="sxs-lookup"><span data-stu-id="1d589-116">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="1d589-117">Qubits: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="1d589-117">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="1d589-118">Der Qubit-Registrierungsstatus wird im Little-Endian-Format registriert.</span><span class="sxs-lookup"><span data-stu-id="1d589-118">Qubit register encoding number states in little-endian format.</span></span> <span data-ttu-id="1d589-119">Diese Initialisierung wird im Berechnungsbasis Status $ \ket{0...0} $ erwartet.</span><span class="sxs-lookup"><span data-stu-id="1d589-119">This is expected to be initialized in the computational basis state $\ket{0...0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1d589-120">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1d589-120">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="1d589-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1d589-121">Remarks</span></span>

<span data-ttu-id="1d589-122">Negative Eingabe Koeffizienten $r _J < $0 werden als positiv mit dem Wert $ | r_j | $ behandelt.</span><span class="sxs-lookup"><span data-stu-id="1d589-122">Negative input coefficients $r_j < 0$ will be treated as though positive with value $|r_j|$.</span></span> <span data-ttu-id="1d589-123">`coefficients` wird mit den Elementen $ (r_j, t_j) = (0,0, 0,0) $ aufgefüllt, wenn weniger als $2 ^ n $ angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1d589-123">`coefficients` will be padded with elements $(r_j, t_j) = (0.0, 0.0)$ if fewer than $2^n$ are specified.</span></span>

## <a name="references"></a><span data-ttu-id="1d589-124">References</span><span class="sxs-lookup"><span data-stu-id="1d589-124">References</span></span>

- <span data-ttu-id="1d589-125">Synthese von Quantum Logic-Leitungen Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span><span class="sxs-lookup"><span data-stu-id="1d589-125">Synthesis of Quantum Logic Circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span></span>
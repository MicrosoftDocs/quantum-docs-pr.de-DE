---
uid: Microsoft.Quantum.Characterization.EstimateRealOverlapBetweenStates
title: Estimaterealoverlapbetweendstates-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: EstimateRealOverlapBetweenStates
qsharp.summary: Given two operations which each prepare copies of a state, estimates the real part of the overlap between the states prepared by each operation.
ms.openlocfilehash: 01631bcbff2bff26ddc1db4e42d90ac4f8380bd4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703613"
---
# <a name="estimaterealoverlapbetweenstates-operation"></a><span data-ttu-id="2d688-102">Estimaterealoverlapbetweendstates-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2d688-102">EstimateRealOverlapBetweenStates operation</span></span>

<span data-ttu-id="2d688-103">Namespace: [Microsoft. Quantum. Charakterisierung](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="2d688-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="2d688-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2d688-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2d688-105">Bei zwei Vorgängen, bei denen Kopien eines Zustands vorbereitet werden, wird der reelle Teil der Überschneidung zwischen den Zuständen, die von jedem Vorgang vorbereitet werden, geschätzt.</span><span class="sxs-lookup"><span data-stu-id="2d688-105">Given two operations which each prepare copies of a state, estimates the real part of the overlap between the states prepared by each operation.</span></span>

```qsharp
operation EstimateRealOverlapBetweenStates (commonPreparation : (Qubit[] => Unit is Adj), preparation1 : (Qubit[] => Unit is Adj + Ctl), preparation2 : (Qubit[] => Unit is Adj + Ctl), nQubits : Int, nMeasurements : Int) : Double
```


## <a name="input"></a><span data-ttu-id="2d688-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2d688-106">Input</span></span>

### <a name="commonpreparation--qubit--unit-adj"></a><span data-ttu-id="2d688-107">commonpreparation: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="2d688-107">commonPreparation : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="2d688-108">Ein Vorgang, der einen festgelegten Eingabe Zustand bereitet.</span><span class="sxs-lookup"><span data-stu-id="2d688-108">An operation that prepares a fixed input state.</span></span>


### <a name="preparation1--qubit--unit-adj--ctl"></a><span data-ttu-id="2d688-109">preparation1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="2d688-109">preparation1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="2d688-110">Der erste der beiden Zustands Vorbereitungs Vorgänge, die verglichen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2d688-110">The first of the two state preparation operations to be compared.</span></span>


### <a name="preparation2--qubit--unit-adj--ctl"></a><span data-ttu-id="2d688-111">preparation2: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="2d688-111">preparation2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="2d688-112">Die zweite der beiden Zustands Vorbereitungs Vorgänge, die verglichen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2d688-112">The second of the two state preparation operations to be compared.</span></span>


### <a name="nqubits--int"></a><span data-ttu-id="2d688-113">nqubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2d688-113">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2d688-114">Die Anzahl der Qubits, für die `commonPreparation` , `preparation1` und `preparation2` alle agieren.</span><span class="sxs-lookup"><span data-stu-id="2d688-114">The number of qubits on which `commonPreparation`, `preparation1`, and `preparation2` all act.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="2d688-115">nmessungen: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2d688-115">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2d688-116">Die Anzahl der Messungen, die beim Schätzen der Überlappung verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2d688-116">The number of measurements to use in estimating the overlap.</span></span>



## <a name="output--double"></a><span data-ttu-id="2d688-117">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="2d688-117">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="remarks"></a><span data-ttu-id="2d688-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2d688-118">Remarks</span></span>

<span data-ttu-id="2d688-119">Bei diesem Vorgang wird der Hadamard-Test verwendet, um den reellen Teil von $ $ \begin{align} \braket{\psi zu suchen. V ^ {\dagger} U | \psi} \end{align} $ $, wobei $ \ket{\psi} $ der von vorbereitete Status ist `commonPreparation` , $U $ die einheitliche Darstellung der Aktion von `preparation1` und wobei $V $ entspricht `preparation2` .</span><span class="sxs-lookup"><span data-stu-id="2d688-119">This operation uses the Hadamard test to find the real part of $$ \begin{align} \braket{\psi | V^{\dagger} U | \psi} \end{align} $$ where $\ket{\psi}$ is the state prepared by `commonPreparation`, $U$ is the unitary representation of the action of `preparation1`, and where $V$ corresponds to `preparation2`.</span></span>

## <a name="references"></a><span data-ttu-id="2d688-120">Referenzen</span><span class="sxs-lookup"><span data-stu-id="2d688-120">References</span></span>

- <span data-ttu-id="2d688-121">Aharonov *et al.* [quant-ph/0511096](https://arxiv.org/abs/quant-ph/0511096).</span><span class="sxs-lookup"><span data-stu-id="2d688-121">Aharonov *et al.* [quant-ph/0511096](https://arxiv.org/abs/quant-ph/0511096).</span></span>

## <a name="see-also"></a><span data-ttu-id="2d688-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2d688-122">See Also</span></span>

- [<span data-ttu-id="2d688-123">Microsoft. Quantum. Charakteri. estimateimagoverlapbetweendstates</span><span class="sxs-lookup"><span data-stu-id="2d688-123">Microsoft.Quantum.Characterization.EstimateImagOverlapBetweenStates</span></span>](xref:Microsoft.Quantum.Characterization.EstimateImagOverlapBetweenStates)
- [<span data-ttu-id="2d688-124">Microsoft. Quantum. Charakterisierung. estimateoverlapbetweendstates</span><span class="sxs-lookup"><span data-stu-id="2d688-124">Microsoft.Quantum.Characterization.EstimateOverlapBetweenStates</span></span>](xref:Microsoft.Quantum.Characterization.EstimateOverlapBetweenStates)
---
uid: Microsoft.Quantum.Characterization.EstimateRealOverlapBetweenStates
title: Estimaterealoverlapbetweendstates-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: EstimateRealOverlapBetweenStates
qsharp.summary: Given two operations which each prepare copies of a state, estimates the real part of the overlap between the states prepared by each operation.
ms.openlocfilehash: 1448e760294e958b152f4ceb3faf979441ca986d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851850"
---
# <a name="estimaterealoverlapbetweenstates-operation"></a><span data-ttu-id="4ee21-102">Estimaterealoverlapbetweendstates-Vorgang</span><span class="sxs-lookup"><span data-stu-id="4ee21-102">EstimateRealOverlapBetweenStates operation</span></span>

<span data-ttu-id="4ee21-103">Namespace: [Microsoft. Quantum. Charakterisierung](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="4ee21-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="4ee21-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4ee21-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4ee21-105">Bei zwei Vorgängen, bei denen Kopien eines Zustands vorbereitet werden, wird der reelle Teil der Überschneidung zwischen den Zuständen, die von jedem Vorgang vorbereitet werden, geschätzt.</span><span class="sxs-lookup"><span data-stu-id="4ee21-105">Given two operations which each prepare copies of a state, estimates the real part of the overlap between the states prepared by each operation.</span></span>

```qsharp
operation EstimateRealOverlapBetweenStates (commonPreparation : (Qubit[] => Unit is Adj), preparation1 : (Qubit[] => Unit is Adj + Ctl), preparation2 : (Qubit[] => Unit is Adj + Ctl), nQubits : Int, nMeasurements : Int) : Double
```


## <a name="input"></a><span data-ttu-id="4ee21-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4ee21-106">Input</span></span>

### <a name="commonpreparation--qubit--unit--is-adj"></a><span data-ttu-id="4ee21-107">commonpreparation: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="4ee21-107">commonPreparation : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="4ee21-108">Ein Vorgang, der einen festgelegten Eingabe Zustand bereitet.</span><span class="sxs-lookup"><span data-stu-id="4ee21-108">An operation that prepares a fixed input state.</span></span>


### <a name="preparation1--qubit--unit--is-adj--ctl"></a><span data-ttu-id="4ee21-109">preparation1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="4ee21-109">preparation1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="4ee21-110">Der erste der beiden Zustands Vorbereitungs Vorgänge, die verglichen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4ee21-110">The first of the two state preparation operations to be compared.</span></span>


### <a name="preparation2--qubit--unit--is-adj--ctl"></a><span data-ttu-id="4ee21-111">preparation2: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="4ee21-111">preparation2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="4ee21-112">Die zweite der beiden Zustands Vorbereitungs Vorgänge, die verglichen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4ee21-112">The second of the two state preparation operations to be compared.</span></span>


### <a name="nqubits--int"></a><span data-ttu-id="4ee21-113">nqubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4ee21-113">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="4ee21-114">Die Anzahl der Qubits, für die `commonPreparation` , `preparation1` und `preparation2` alle agieren.</span><span class="sxs-lookup"><span data-stu-id="4ee21-114">The number of qubits on which `commonPreparation`, `preparation1`, and `preparation2` all act.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="4ee21-115">nmessungen: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4ee21-115">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="4ee21-116">Die Anzahl der Messungen, die beim Schätzen der Überlappung verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4ee21-116">The number of measurements to use in estimating the overlap.</span></span>



## <a name="output--double"></a><span data-ttu-id="4ee21-117">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="4ee21-117">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="remarks"></a><span data-ttu-id="4ee21-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4ee21-118">Remarks</span></span>

<span data-ttu-id="4ee21-119">Bei diesem Vorgang wird der Hadamard-Test verwendet, um den reellen Teil von $ $ \begin{align} \braket{\psi zu suchen. V ^ {\dagger} U | \psi} \end{align} $ $, wobei $ \ket{\psi} $ der von vorbereitete Status ist `commonPreparation` , $U $ die einheitliche Darstellung der Aktion von `preparation1` und wobei $V $ entspricht `preparation2` .</span><span class="sxs-lookup"><span data-stu-id="4ee21-119">This operation uses the Hadamard test to find the real part of $$ \begin{align} \braket{\psi | V^{\dagger} U | \psi} \end{align} $$ where $\ket{\psi}$ is the state prepared by `commonPreparation`, $U$ is the unitary representation of the action of `preparation1`, and where $V$ corresponds to `preparation2`.</span></span>

## <a name="references"></a><span data-ttu-id="4ee21-120">References</span><span class="sxs-lookup"><span data-stu-id="4ee21-120">References</span></span>

- <span data-ttu-id="4ee21-121">Aharonov *et al.* [quant-ph/0511096](https://arxiv.org/abs/quant-ph/0511096).</span><span class="sxs-lookup"><span data-stu-id="4ee21-121">Aharonov *et al.* [quant-ph/0511096](https://arxiv.org/abs/quant-ph/0511096).</span></span>

## <a name="see-also"></a><span data-ttu-id="4ee21-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4ee21-122">See Also</span></span>

- [<span data-ttu-id="4ee21-123">Microsoft. Quantum. Charakteri. estimateimagoverlapbetweendstates</span><span class="sxs-lookup"><span data-stu-id="4ee21-123">Microsoft.Quantum.Characterization.EstimateImagOverlapBetweenStates</span></span>](xref:Microsoft.Quantum.Characterization.EstimateImagOverlapBetweenStates)
- [<span data-ttu-id="4ee21-124">Microsoft. Quantum. Charakterisierung. estimateoverlapbetweendstates</span><span class="sxs-lookup"><span data-stu-id="4ee21-124">Microsoft.Quantum.Characterization.EstimateOverlapBetweenStates</span></span>](xref:Microsoft.Quantum.Characterization.EstimateOverlapBetweenStates)
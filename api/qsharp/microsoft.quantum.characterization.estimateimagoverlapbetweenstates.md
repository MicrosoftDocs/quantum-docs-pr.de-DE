---
uid: Microsoft.Quantum.Characterization.EstimateImagOverlapBetweenStates
title: Estimateimagoverlapbetweendstates-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: EstimateImagOverlapBetweenStates
qsharp.summary: Given two operations which each prepare copies of a state, estimates the imaginary part of the overlap between the states prepared by each operation.
ms.openlocfilehash: f18ce43f9e5ebada4c5cc0aeff1538ac640c7390
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851864"
---
# <a name="estimateimagoverlapbetweenstates-operation"></a><span data-ttu-id="85395-102">Estimateimagoverlapbetweendstates-Vorgang</span><span class="sxs-lookup"><span data-stu-id="85395-102">EstimateImagOverlapBetweenStates operation</span></span>

<span data-ttu-id="85395-103">Namespace: [Microsoft. Quantum. Charakterisierung](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="85395-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="85395-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="85395-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="85395-105">Bei zwei Vorgängen, bei denen die Kopien eines Zustands vorbereitet werden, wird der Imaginärteil der Überschneidung zwischen den Zuständen, die von jedem Vorgang vorbereitet werden, geschätzt.</span><span class="sxs-lookup"><span data-stu-id="85395-105">Given two operations which each prepare copies of a state, estimates the imaginary part of the overlap between the states prepared by each operation.</span></span>

```qsharp
operation EstimateImagOverlapBetweenStates (commonPreparation : (Qubit[] => Unit is Adj), preparation1 : (Qubit[] => Unit is Adj + Ctl), preparation2 : (Qubit[] => Unit is Adj + Ctl), nQubits : Int, nMeasurements : Int) : Double
```


## <a name="input"></a><span data-ttu-id="85395-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="85395-106">Input</span></span>

### <a name="commonpreparation--qubit--unit--is-adj"></a><span data-ttu-id="85395-107">commonpreparation: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="85395-107">commonPreparation : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="85395-108">Ein Vorgang, der einen festgelegten Eingabe Zustand bereitet.</span><span class="sxs-lookup"><span data-stu-id="85395-108">An operation that prepares a fixed input state.</span></span>


### <a name="preparation1--qubit--unit--is-adj--ctl"></a><span data-ttu-id="85395-109">preparation1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="85395-109">preparation1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="85395-110">Der erste der beiden Zustands Vorbereitungs Vorgänge, die verglichen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="85395-110">The first of the two state preparation operations to be compared.</span></span>


### <a name="preparation2--qubit--unit--is-adj--ctl"></a><span data-ttu-id="85395-111">preparation2: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="85395-111">preparation2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="85395-112">Die zweite der beiden Zustands Vorbereitungs Vorgänge, die verglichen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="85395-112">The second of the two state preparation operations to be compared.</span></span>


### <a name="nqubits--int"></a><span data-ttu-id="85395-113">nqubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="85395-113">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="85395-114">Die Anzahl der Qubits, für die `commonPreparation` , `preparation1` und `preparation2` alle agieren.</span><span class="sxs-lookup"><span data-stu-id="85395-114">The number of qubits on which `commonPreparation`, `preparation1`, and `preparation2` all act.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="85395-115">nmessungen: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="85395-115">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="85395-116">Die Anzahl der Messungen, die beim Schätzen der Überlappung verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="85395-116">The number of measurements to use in estimating the overlap.</span></span>



## <a name="output--double"></a><span data-ttu-id="85395-117">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="85395-117">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="remarks"></a><span data-ttu-id="85395-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="85395-118">Remarks</span></span>

<span data-ttu-id="85395-119">Bei diesem Vorgang wird der Hadamard-Test verwendet, um den imaginären Teil von $ $ \begin{align} \braket{\psi zu suchen. V ^ {\dagger} U | \psi} \end{align} $ $, wobei $ \ket{\psi} $ der von vorbereitete Status ist `commonPreparation` , $U $ die einheitliche Darstellung der Aktion von `preparation1` und wobei $V $ entspricht `preparation2` .</span><span class="sxs-lookup"><span data-stu-id="85395-119">This operation uses the Hadamard test to find the imaginary part of $$ \begin{align} \braket{\psi | V^{\dagger} U | \psi} \end{align} $$ where $\ket{\psi}$ is the state prepared by `commonPreparation`, $U$ is the unitary representation of the action of `preparation1`, and where $V$ corresponds to `preparation2`.</span></span>

## <a name="references"></a><span data-ttu-id="85395-120">References</span><span class="sxs-lookup"><span data-stu-id="85395-120">References</span></span>

- <span data-ttu-id="85395-121">Aharonov *et al.* [quant-ph/0511096](https://arxiv.org/abs/quant-ph/0511096).</span><span class="sxs-lookup"><span data-stu-id="85395-121">Aharonov *et al.* [quant-ph/0511096](https://arxiv.org/abs/quant-ph/0511096).</span></span>

## <a name="see-also"></a><span data-ttu-id="85395-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="85395-122">See Also</span></span>

- [<span data-ttu-id="85395-123">Microsoft. Quantum. Charakterisierung. estimaterealoverlapbetweerstates</span><span class="sxs-lookup"><span data-stu-id="85395-123">Microsoft.Quantum.Characterization.EstimateRealOverlapBetweenStates</span></span>](xref:Microsoft.Quantum.Characterization.EstimateRealOverlapBetweenStates)
- [<span data-ttu-id="85395-124">Microsoft. Quantum. Charakterisierung. estimateoverlapbetweendstates</span><span class="sxs-lookup"><span data-stu-id="85395-124">Microsoft.Quantum.Characterization.EstimateOverlapBetweenStates</span></span>](xref:Microsoft.Quantum.Characterization.EstimateOverlapBetweenStates)
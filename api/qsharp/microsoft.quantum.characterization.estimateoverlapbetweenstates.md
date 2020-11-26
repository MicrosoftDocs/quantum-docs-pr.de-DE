---
uid: Microsoft.Quantum.Characterization.EstimateOverlapBetweenStates
title: Estimateoverlapbetweendstates-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: EstimateOverlapBetweenStates
qsharp.summary: Given two operations which each prepare copies of a state, estimates the squared overlap between the states prepared by each operation.
ms.openlocfilehash: 07693ccf4b8e7bbde189674d9e6b2bf7f92222f6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204299"
---
# <a name="estimateoverlapbetweenstates-operation"></a><span data-ttu-id="5a3c6-102">Estimateoverlapbetweendstates-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5a3c6-102">EstimateOverlapBetweenStates operation</span></span>

<span data-ttu-id="5a3c6-103">Namespace: [Microsoft. Quantum. Charakterisierung](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="5a3c6-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="5a3c6-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5a3c6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5a3c6-105">Bei zwei Vorgängen, bei denen Kopien eines Zustands vorbereitet werden, wird die Quadrat Überschneidung zwischen den von jedem Vorgang vorbereiteten Zuständen geschätzt.</span><span class="sxs-lookup"><span data-stu-id="5a3c6-105">Given two operations which each prepare copies of a state, estimates the squared overlap between the states prepared by each operation.</span></span>

```qsharp
operation EstimateOverlapBetweenStates (preparation1 : (Qubit[] => Unit is Adj), preparation2 : (Qubit[] => Unit is Adj), nQubits : Int, nMeasurements : Int) : Double
```


## <a name="input"></a><span data-ttu-id="5a3c6-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5a3c6-106">Input</span></span>

### <a name="preparation1--qubit--unit--is-adj"></a><span data-ttu-id="5a3c6-107">preparation1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="5a3c6-107">preparation1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="5a3c6-108">Der erste der beiden Zustands Vorbereitungs Vorgänge, die verglichen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5a3c6-108">The first of the two state preparation operations to be compared.</span></span>


### <a name="preparation2--qubit--unit--is-adj"></a><span data-ttu-id="5a3c6-109">preparation2: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="5a3c6-109">preparation2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="5a3c6-110">Die zweite der beiden Zustands Vorbereitungs Vorgänge, die verglichen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5a3c6-110">The second of the two state preparation operations to be compared.</span></span>


### <a name="nqubits--int"></a><span data-ttu-id="5a3c6-111">nqubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5a3c6-111">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5a3c6-112">Die Anzahl der Qubits, für die `commonPreparation` , `preparation1` und `preparation2` alle agieren.</span><span class="sxs-lookup"><span data-stu-id="5a3c6-112">The number of qubits on which `commonPreparation`, `preparation1`, and `preparation2` all act.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="5a3c6-113">nmessungen: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5a3c6-113">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5a3c6-114">Die Anzahl der Messungen, die beim Schätzen der Überlappung verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5a3c6-114">The number of measurements to use in estimating the overlap.</span></span>



## <a name="output--double"></a><span data-ttu-id="5a3c6-115">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="5a3c6-115">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>



## <a name="remarks"></a><span data-ttu-id="5a3c6-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5a3c6-116">Remarks</span></span>

<span data-ttu-id="5a3c6-117">Bei diesem Vorgang wird der Swap-Test verwendet, um $ $ \begin{align} \left | \braket{00\cdots 0 | V ^ {\dagger} U | 00 \ cdots 0} \right | ^ 2 \end{align} $ $, wobei $U $ die einheitliche Darstellung der Aktion von `preparation1` und wobei $V $ entspricht `preparation2` .</span><span class="sxs-lookup"><span data-stu-id="5a3c6-117">This operation uses the SWAP test to find $$ \begin{align} \left| \braket{00\cdots 0 | V^{\dagger} U | 00\cdots 0} \right|^2 \end{align} $$ where $U$ is the unitary representation of the action of `preparation1`, and where $V$ corresponds to `preparation2`.</span></span>

## <a name="see-also"></a><span data-ttu-id="5a3c6-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5a3c6-118">See Also</span></span>

- [<span data-ttu-id="5a3c6-119">Microsoft. Quantum. Charakterisierung. estimaterealoverlapbetweerstates</span><span class="sxs-lookup"><span data-stu-id="5a3c6-119">Microsoft.Quantum.Characterization.EstimateRealOverlapBetweenStates</span></span>](xref:Microsoft.Quantum.Characterization.EstimateRealOverlapBetweenStates)
- [<span data-ttu-id="5a3c6-120">Microsoft. Quantum. Charakteri. estimateimagoverlapbetweendstates</span><span class="sxs-lookup"><span data-stu-id="5a3c6-120">Microsoft.Quantum.Characterization.EstimateImagOverlapBetweenStates</span></span>](xref:Microsoft.Quantum.Characterization.EstimateImagOverlapBetweenStates)
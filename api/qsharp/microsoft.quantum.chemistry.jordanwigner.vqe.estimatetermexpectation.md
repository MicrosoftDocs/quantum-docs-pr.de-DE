---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.EstimateTermExpectation
title: Estimatetermexpectation-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: EstimateTermExpectation
qsharp.summary: Computes the energy associated to a given Jordan-Wigner Hamiltonian term
ms.openlocfilehash: ef689c55f966e63a2ab8bcdccf99d9cb5e6d3a4d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703079"
---
# <a name="estimatetermexpectation-operation"></a><span data-ttu-id="814b1-102">Estimatetermexpectation-Vorgang</span><span class="sxs-lookup"><span data-stu-id="814b1-102">EstimateTermExpectation operation</span></span>

<span data-ttu-id="814b1-103">Namespace: [Microsoft. Quantum. Chemistry. jordanwigner. vqe](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span><span class="sxs-lookup"><span data-stu-id="814b1-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner.VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span></span>

<span data-ttu-id="814b1-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="814b1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="814b1-105">Berechnet die Energie, die einem angegebenen Jordan-Wigner hamiltona-Begriff zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="814b1-105">Computes the energy associated to a given Jordan-Wigner Hamiltonian term</span></span>

```qsharp
operation EstimateTermExpectation (inputStateUnitary : (Qubit[] => Unit is Adj), ops : Pauli[][], coeffs : Double[], nQubits : Int, nSamples : Int) : Double
```


## <a name="description"></a><span data-ttu-id="814b1-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="814b1-106">Description</span></span>

<span data-ttu-id="814b1-107">Mit diesem Vorgang wird der Erwartungswert geschätzt, der jedem Mess Operator zugeordnet ist, und der Wert wird mithilfe von Sampling mit dem entsprechenden Koeffizienten multipliziert.</span><span class="sxs-lookup"><span data-stu-id="814b1-107">This operation estimates the expectation value associated to each measurement operator and multiplies it by the corresponding coefficient, using sampling.</span></span>
<span data-ttu-id="814b1-108">Die Ergebnisse werden in eine Variable aggregiert, die die Energie des Jordan-Wigner Begriffs enthält.</span><span class="sxs-lookup"><span data-stu-id="814b1-108">The results are aggregated into a variable containing the energy of the Jordan-Wigner term.</span></span>

## <a name="input"></a><span data-ttu-id="814b1-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="814b1-109">Input</span></span>

### <a name="inputstateunitary--qubit--unit-adj"></a><span data-ttu-id="814b1-110">inputstateeinheitliches: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="814b1-110">inputStateUnitary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="814b1-111">Der für die Zustands Vorbereitung verwendete einheitliche.</span><span class="sxs-lookup"><span data-stu-id="814b1-111">The unitary used for state preparation.</span></span>


### <a name="ops--pauli"></a><span data-ttu-id="814b1-112">OPS: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="814b1-112">ops : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="814b1-113">Die maßoperatoren des Jordan-Wigner Begriffs.</span><span class="sxs-lookup"><span data-stu-id="814b1-113">The measurement operators of the Jordan-Wigner term.</span></span>


### <a name="coeffs--double"></a><span data-ttu-id="814b1-114">coeffs: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="814b1-114">coeffs : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="814b1-115">Die Koeffizienten des Jordan-Wigner Begriffs.</span><span class="sxs-lookup"><span data-stu-id="814b1-115">The coefficients of the Jordan-Wigner term.</span></span>


### <a name="nqubits--int"></a><span data-ttu-id="814b1-116">nqubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="814b1-116">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="814b1-117">Die Anzahl der zum Simulieren des molekularen Systems erforderlichen Qubits.</span><span class="sxs-lookup"><span data-stu-id="814b1-117">The number of qubits required to simulate the molecular system.</span></span>


### <a name="nsamples--int"></a><span data-ttu-id="814b1-118">nsamples: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="814b1-118">nSamples : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="814b1-119">Die Anzahl der Samplings, die für die Schätzung der Begriffs Erwartung verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="814b1-119">The number of samples to use for the estimation of the term expectation.</span></span>



## <a name="output--double"></a><span data-ttu-id="814b1-120">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="814b1-120">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="814b1-121">Die dem Jordan-Wigner Begriff zugeordnete Energie.</span><span class="sxs-lookup"><span data-stu-id="814b1-121">The energy associated to the Jordan-Wigner term.</span></span>
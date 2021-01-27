---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.EstimateTermExpectation
title: Estimatetermexpectation-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: EstimateTermExpectation
qsharp.summary: Computes the energy associated to a given Jordan-Wigner Hamiltonian term
ms.openlocfilehash: 7df4c1ea859140a669698434c6f8a786ea3bc2ea
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98835672"
---
# <a name="estimatetermexpectation-operation"></a><span data-ttu-id="34589-102">Estimatetermexpectation-Vorgang</span><span class="sxs-lookup"><span data-stu-id="34589-102">EstimateTermExpectation operation</span></span>

<span data-ttu-id="34589-103">Namespace: [Microsoft. Quantum. Chemistry. jordanwigner. vqe](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span><span class="sxs-lookup"><span data-stu-id="34589-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner.VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span></span>

<span data-ttu-id="34589-104">Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="34589-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="34589-105">Berechnet die Energie, die einem angegebenen Jordan-Wigner hamiltona-Begriff zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="34589-105">Computes the energy associated to a given Jordan-Wigner Hamiltonian term</span></span>

```qsharp
operation EstimateTermExpectation (inputStateUnitary : (Qubit[] => Unit is Adj), ops : Pauli[][], coeffs : Double[], nQubits : Int, nSamples : Int) : Double
```


## <a name="description"></a><span data-ttu-id="34589-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="34589-106">Description</span></span>

<span data-ttu-id="34589-107">Mit diesem Vorgang wird der Erwartungswert geschätzt, der jedem Mess Operator zugeordnet ist, und der Wert wird mithilfe von Sampling mit dem entsprechenden Koeffizienten multipliziert.</span><span class="sxs-lookup"><span data-stu-id="34589-107">This operation estimates the expectation value associated to each measurement operator and multiplies it by the corresponding coefficient, using sampling.</span></span>
<span data-ttu-id="34589-108">Die Ergebnisse werden in eine Variable aggregiert, die die Energie des Jordan-Wigner Begriffs enthält.</span><span class="sxs-lookup"><span data-stu-id="34589-108">The results are aggregated into a variable containing the energy of the Jordan-Wigner term.</span></span>

## <a name="input"></a><span data-ttu-id="34589-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34589-109">Input</span></span>

### <a name="inputstateunitary--qubit--unit--is-adj"></a><span data-ttu-id="34589-110">inputstateeinheitliches: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ</span><span class="sxs-lookup"><span data-stu-id="34589-110">inputStateUnitary : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="34589-111">Der für die Zustands Vorbereitung verwendete einheitliche.</span><span class="sxs-lookup"><span data-stu-id="34589-111">The unitary used for state preparation.</span></span>


### <a name="ops--pauli"></a><span data-ttu-id="34589-112">OPS: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="34589-112">ops : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="34589-113">Die maßoperatoren des Jordan-Wigner Begriffs.</span><span class="sxs-lookup"><span data-stu-id="34589-113">The measurement operators of the Jordan-Wigner term.</span></span>


### <a name="coeffs--double"></a><span data-ttu-id="34589-114">coeffs: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="34589-114">coeffs : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="34589-115">Die Koeffizienten des Jordan-Wigner Begriffs.</span><span class="sxs-lookup"><span data-stu-id="34589-115">The coefficients of the Jordan-Wigner term.</span></span>


### <a name="nqubits--int"></a><span data-ttu-id="34589-116">nqubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="34589-116">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="34589-117">Die Anzahl der zum Simulieren des molekularen Systems erforderlichen Qubits.</span><span class="sxs-lookup"><span data-stu-id="34589-117">The number of qubits required to simulate the molecular system.</span></span>


### <a name="nsamples--int"></a><span data-ttu-id="34589-118">nsamples: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="34589-118">nSamples : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="34589-119">Die Anzahl der Samplings, die für die Schätzung der Begriffs Erwartung verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="34589-119">The number of samples to use for the estimation of the term expectation.</span></span>



## <a name="output--double"></a><span data-ttu-id="34589-120">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="34589-120">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="34589-121">Die dem Jordan-Wigner Begriff zugeordnete Energie.</span><span class="sxs-lookup"><span data-stu-id="34589-121">The energy associated to the Jordan-Wigner term.</span></span>
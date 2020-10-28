---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.EstimateEnergy
title: Estimateenergy-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: EstimateEnergy
qsharp.summary: Estimates the energy of the molecule by summing the energy contributed by the individual Jordan-Wigner terms.
ms.openlocfilehash: 52e527a68818c80f93bc177d3563064fd0f2aea3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703086"
---
# <a name="estimateenergy-operation"></a><span data-ttu-id="a96a5-102">Estimateenergy-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a96a5-102">EstimateEnergy operation</span></span>

<span data-ttu-id="a96a5-103">Namespace: [Microsoft. Quantum. Chemistry. jordanwigner. vqe](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span><span class="sxs-lookup"><span data-stu-id="a96a5-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner.VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span></span>

<span data-ttu-id="a96a5-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a96a5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a96a5-105">Schätzt die Energie des Moleküls, indem die von den einzelnen Jordan-Wigner Begriffen beigetragene Energie summiert wird.</span><span class="sxs-lookup"><span data-stu-id="a96a5-105">Estimates the energy of the molecule by summing the energy contributed by the individual Jordan-Wigner terms.</span></span>

```qsharp
operation EstimateEnergy (jwHamiltonian : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData, nSamples : Int) : Double
```


## <a name="description"></a><span data-ttu-id="a96a5-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a96a5-106">Description</span></span>

<span data-ttu-id="a96a5-107">Dieser Vorgang basiert implizit auf der Indizierungs Konvention für die Aufgliederung.</span><span class="sxs-lookup"><span data-stu-id="a96a5-107">This operation implicitly relies on the spin up-down indexing convention.</span></span>

## <a name="input"></a><span data-ttu-id="a96a5-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a96a5-108">Input</span></span>

### <a name="jwhamiltonian--jordanwignerencodingdata"></a><span data-ttu-id="a96a5-109">jwhamiltonan: [jordanwignerencodingdata](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)</span><span class="sxs-lookup"><span data-stu-id="a96a5-109">jwHamiltonian : [JordanWignerEncodingData](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)</span></span>

<span data-ttu-id="a96a5-110">Der Jordan-Wigner hamiltonan.</span><span class="sxs-lookup"><span data-stu-id="a96a5-110">The Jordan-Wigner Hamiltonian.</span></span>


### <a name="nsamples--int"></a><span data-ttu-id="a96a5-111">nsamples: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a96a5-111">nSamples : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a96a5-112">Die Anzahl der Samplings, die für die Schätzung der Begriffs Erwartungen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a96a5-112">The number of samples to use for the estimation of the term expectations.</span></span>



## <a name="output--double"></a><span data-ttu-id="a96a5-113">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="a96a5-113">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="a96a5-114">Die geschätzte Energie des Moleküls</span><span class="sxs-lookup"><span data-stu-id="a96a5-114">The estimated energy of the molecule</span></span>
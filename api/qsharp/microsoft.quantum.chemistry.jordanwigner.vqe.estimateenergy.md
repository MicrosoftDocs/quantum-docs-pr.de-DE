---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE.EstimateEnergy
title: Estimateenergy-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: EstimateEnergy
qsharp.summary: Estimates the energy of the molecule by summing the energy contributed by the individual Jordan-Wigner terms.
ms.openlocfilehash: a64ac3970e3e67568f91b4e67775d834a80c04a1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98835728"
---
# <a name="estimateenergy-operation"></a><span data-ttu-id="d5e9a-102">Estimateenergy-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d5e9a-102">EstimateEnergy operation</span></span>

<span data-ttu-id="d5e9a-103">Namespace: [Microsoft. Quantum. Chemistry. jordanwigner. vqe](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span><span class="sxs-lookup"><span data-stu-id="d5e9a-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner.VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span></span>

<span data-ttu-id="d5e9a-104">Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="d5e9a-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="d5e9a-105">Schätzt die Energie des Moleküls, indem die von den einzelnen Jordan-Wigner Begriffen beigetragene Energie summiert wird.</span><span class="sxs-lookup"><span data-stu-id="d5e9a-105">Estimates the energy of the molecule by summing the energy contributed by the individual Jordan-Wigner terms.</span></span>

```qsharp
operation EstimateEnergy (jwHamiltonian : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData, nSamples : Int) : Double
```


## <a name="description"></a><span data-ttu-id="d5e9a-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d5e9a-106">Description</span></span>

<span data-ttu-id="d5e9a-107">Dieser Vorgang basiert implizit auf der Indizierungs Konvention für die Aufgliederung.</span><span class="sxs-lookup"><span data-stu-id="d5e9a-107">This operation implicitly relies on the spin up-down indexing convention.</span></span>

## <a name="input"></a><span data-ttu-id="d5e9a-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d5e9a-108">Input</span></span>

### <a name="jwhamiltonian--jordanwignerencodingdata"></a><span data-ttu-id="d5e9a-109">jwhamiltonan: [jordanwignerencodingdata](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)</span><span class="sxs-lookup"><span data-stu-id="d5e9a-109">jwHamiltonian : [JordanWignerEncodingData](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)</span></span>

<span data-ttu-id="d5e9a-110">Der Jordan-Wigner hamiltonan.</span><span class="sxs-lookup"><span data-stu-id="d5e9a-110">The Jordan-Wigner Hamiltonian.</span></span>


### <a name="nsamples--int"></a><span data-ttu-id="d5e9a-111">nsamples: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d5e9a-111">nSamples : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d5e9a-112">Die Anzahl der Samplings, die für die Schätzung der Begriffs Erwartungen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d5e9a-112">The number of samples to use for the estimation of the term expectations.</span></span>



## <a name="output--double"></a><span data-ttu-id="d5e9a-113">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="d5e9a-113">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="d5e9a-114">Die geschätzte Energie des Moleküls</span><span class="sxs-lookup"><span data-stu-id="d5e9a-114">The estimated energy of the molecule</span></span>
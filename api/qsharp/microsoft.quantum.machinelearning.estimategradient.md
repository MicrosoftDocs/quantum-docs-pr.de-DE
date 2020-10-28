---
uid: Microsoft.Quantum.MachineLearning.EstimateGradient
title: Estimategradient-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: EstimateGradient
qsharp.summary: Estimates the training gradient for a sequential classifier at a particular model and for a given encoded input.
ms.openlocfilehash: f42cc30c98346a25f584d7527227a95cb413c32b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706511"
---
# <a name="estimategradient-operation"></a><span data-ttu-id="67850-102">Estimategradient-Vorgang</span><span class="sxs-lookup"><span data-stu-id="67850-102">EstimateGradient operation</span></span>

<span data-ttu-id="67850-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="67850-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="67850-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="67850-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="67850-105">Schätzt den Trainingsverlauf für einen sequenziellen Klassifizierer bei einem bestimmten Modell und für eine bestimmte codierte Eingabe.</span><span class="sxs-lookup"><span data-stu-id="67850-105">Estimates the training gradient for a sequential classifier at a particular model and for a given encoded input.</span></span>

```qsharp
operation EstimateGradient (model : Microsoft.Quantum.MachineLearning.SequentialModel, encodedInput : Microsoft.Quantum.MachineLearning.StateGenerator, nMeasurements : Int) : Double[]
```


## <a name="input"></a><span data-ttu-id="67850-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="67850-106">Input</span></span>

### <a name="model--sequentialmodel"></a><span data-ttu-id="67850-107">Modell: [sequentialmodel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="67850-107">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>

<span data-ttu-id="67850-108">Das sequenzielle Modell, dessen Farbverlauf geschätzt wird.</span><span class="sxs-lookup"><span data-stu-id="67850-108">The sequential model whose gradient is to be estimated.</span></span>


### <a name="encodedinput--stategenerator"></a><span data-ttu-id="67850-109">encodebug: [stategenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span><span class="sxs-lookup"><span data-stu-id="67850-109">encodedInput : [StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span></span>

<span data-ttu-id="67850-110">Eine Eingabe für den sequenziellen Klassifizierer, die in einen Zustands Vorbereitungs Vorgang codiert ist.</span><span class="sxs-lookup"><span data-stu-id="67850-110">An input to the sequential classifier, encoded into a state preparation operation.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="67850-111">nmessungen: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="67850-111">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="67850-112">Die Anzahl der Messungen, die beim Schätzen des Farbverlaufs verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="67850-112">The number of measurements to use in estimating the gradient.</span></span>



## <a name="output--double"></a><span data-ttu-id="67850-113">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="67850-113">Output : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="67850-114">Eine Schätzung des Trainings Farbverlaufs bei den angegebenen Eingabe-und Modellparametern.</span><span class="sxs-lookup"><span data-stu-id="67850-114">An estimate of the training gradient at the given input and model parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="67850-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="67850-115">Remarks</span></span>

<span data-ttu-id="67850-116">Bei diesem Vorgang wird ein Hadamard-Test und die Parameter Verschiebungs Technik verwendet, um den Farbverlauf zu schätzen.</span><span class="sxs-lookup"><span data-stu-id="67850-116">This operation uses a Hadamard test and the parameter shift technique together to estimate the gradient.</span></span>
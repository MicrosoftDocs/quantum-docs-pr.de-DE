---
uid: Microsoft.Quantum.MachineLearning.EstimateGradient
title: Estimategradient-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: EstimateGradient
qsharp.summary: Estimates the training gradient for a sequential classifier at a particular model and for a given encoded input.
ms.openlocfilehash: 79f4abdf131509d4948a3c114e631118329f88d8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211847"
---
# <a name="estimategradient-operation"></a><span data-ttu-id="1168c-102">Estimategradient-Vorgang</span><span class="sxs-lookup"><span data-stu-id="1168c-102">EstimateGradient operation</span></span>

<span data-ttu-id="1168c-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="1168c-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="1168c-104">Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="1168c-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="1168c-105">Schätzt den Trainingsverlauf für einen sequenziellen Klassifizierer bei einem bestimmten Modell und für eine bestimmte codierte Eingabe.</span><span class="sxs-lookup"><span data-stu-id="1168c-105">Estimates the training gradient for a sequential classifier at a particular model and for a given encoded input.</span></span>

```qsharp
operation EstimateGradient (model : Microsoft.Quantum.MachineLearning.SequentialModel, encodedInput : Microsoft.Quantum.MachineLearning.StateGenerator, nMeasurements : Int) : Double[]
```


## <a name="input"></a><span data-ttu-id="1168c-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1168c-106">Input</span></span>

### <a name="model--sequentialmodel"></a><span data-ttu-id="1168c-107">Modell: [sequentialmodel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="1168c-107">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>

<span data-ttu-id="1168c-108">Das sequenzielle Modell, dessen Farbverlauf geschätzt wird.</span><span class="sxs-lookup"><span data-stu-id="1168c-108">The sequential model whose gradient is to be estimated.</span></span>


### <a name="encodedinput--stategenerator"></a><span data-ttu-id="1168c-109">encodebug: [stategenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span><span class="sxs-lookup"><span data-stu-id="1168c-109">encodedInput : [StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span></span>

<span data-ttu-id="1168c-110">Eine Eingabe für den sequenziellen Klassifizierer, die in einen Zustands Vorbereitungs Vorgang codiert ist.</span><span class="sxs-lookup"><span data-stu-id="1168c-110">An input to the sequential classifier, encoded into a state preparation operation.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="1168c-111">nmessungen: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="1168c-111">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="1168c-112">Die Anzahl der Messungen, die beim Schätzen des Farbverlaufs verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1168c-112">The number of measurements to use in estimating the gradient.</span></span>



## <a name="output--double"></a><span data-ttu-id="1168c-113">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="1168c-113">Output : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="1168c-114">Eine Schätzung des Trainings Farbverlaufs bei den angegebenen Eingabe-und Modellparametern.</span><span class="sxs-lookup"><span data-stu-id="1168c-114">An estimate of the training gradient at the given input and model parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="1168c-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1168c-115">Remarks</span></span>

<span data-ttu-id="1168c-116">Bei diesem Vorgang wird ein Hadamard-Test und die Parameter Verschiebungs Technik verwendet, um den Farbverlauf zu schätzen.</span><span class="sxs-lookup"><span data-stu-id="1168c-116">This operation uses a Hadamard test and the parameter shift technique together to estimate the gradient.</span></span>
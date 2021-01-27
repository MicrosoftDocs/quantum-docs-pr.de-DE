---
uid: Microsoft.Quantum.MachineLearning.EstimateClassificationProbabilities
title: Estimateclassificationprobabiliesoperation
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: EstimateClassificationProbabilities
qsharp.summary: Given a set of samples and a sequential classifier, estimates the classification probability for those samples by repeatedly measuring the output of the classifier on each sample.
ms.openlocfilehash: eea503d042d6ffc241186c117a7c02ee72983b09
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847717"
---
# <a name="estimateclassificationprobabilities-operation"></a><span data-ttu-id="a9efc-102">Estimateclassificationprobabiliesoperation</span><span class="sxs-lookup"><span data-stu-id="a9efc-102">EstimateClassificationProbabilities operation</span></span>

<span data-ttu-id="a9efc-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="a9efc-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="a9efc-104">Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="a9efc-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="a9efc-105">Bei einer Reihe von Beispielen und einem sequenziellen Klassifizierer wird die Klassifizierungs Wahrscheinlichkeit für diese Stichproben durch wiederholtes Messen der Ausgabe des Klassifizierers in den einzelnen Stichproben geschätzt.</span><span class="sxs-lookup"><span data-stu-id="a9efc-105">Given a set of samples and a sequential classifier, estimates the classification probability for those samples by repeatedly measuring the output of the classifier on each sample.</span></span>

```qsharp
operation EstimateClassificationProbabilities (tolerance : Double, model : Microsoft.Quantum.MachineLearning.SequentialModel, samples : Double[][], nMeasurements : Int) : Double[]
```


## <a name="input"></a><span data-ttu-id="a9efc-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a9efc-106">Input</span></span>

### <a name="tolerance--double"></a><span data-ttu-id="a9efc-107">Toleranz: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="a9efc-107">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="a9efc-108">Die Toleranz, die das Codieren des Beispiels in einen Zustands Vorbereitungs Vorgang zulässt.</span><span class="sxs-lookup"><span data-stu-id="a9efc-108">The tolerance to allow in encoding the sample into a state preparation operation.</span></span>


### <a name="model--sequentialmodel"></a><span data-ttu-id="a9efc-109">Modell: [sequentialmodel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="a9efc-109">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>

<span data-ttu-id="a9efc-110">Das sequenzielle Modell, das zum Schätzen der Klassifizierungs Wahrscheinlichkeiten für die angegebenen Beispiele verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a9efc-110">The sequential model to be used to estimate the classification probabilities for the given samples.</span></span>


### <a name="samples--double"></a><span data-ttu-id="a9efc-111">Beispiele: [Double](xref:microsoft.quantum.lang-ref.double)[] []</span><span class="sxs-lookup"><span data-stu-id="a9efc-111">samples : [Double](xref:microsoft.quantum.lang-ref.double)[][]</span></span>

<span data-ttu-id="a9efc-112">Ein Array von Merkmals Vektoren für jede zu klassifizierende Stichprobe.</span><span class="sxs-lookup"><span data-stu-id="a9efc-112">An array of feature vectors for each sample to be classified.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="a9efc-113">nmessungen: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a9efc-113">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a9efc-114">Die Anzahl der Messungen, die beim Schätzen der Klassifizierungs Wahrscheinlichkeit verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a9efc-114">The number of measurements to use in estimating the classification probability.</span></span>



## <a name="output--double"></a><span data-ttu-id="a9efc-115">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="a9efc-115">Output : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="a9efc-116">Ein Array von Schätzungen der Klassifizierungs Wahrscheinlichkeit für jedes gegebene Beispiel.</span><span class="sxs-lookup"><span data-stu-id="a9efc-116">An array of estimates of the classification probability for each given sample.</span></span>
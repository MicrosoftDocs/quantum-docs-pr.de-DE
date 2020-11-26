---
uid: Microsoft.Quantum.MachineLearning.EstimateClassificationProbability
title: Estimateclassificationwahrscheinlichkeits-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: EstimateClassificationProbability
qsharp.summary: Given a sample and a sequential classifier, estimates the classification probability for that sample by repeatedly measuring the output of the classifier on the given sample.
ms.openlocfilehash: 9d127bba9624e178fbdb631a1249efe5fc2be3b0
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196462"
---
# <a name="estimateclassificationprobability-operation"></a><span data-ttu-id="33a67-102">Estimateclassificationwahrscheinlichkeits-Vorgang</span><span class="sxs-lookup"><span data-stu-id="33a67-102">EstimateClassificationProbability operation</span></span>

<span data-ttu-id="33a67-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="33a67-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="33a67-104">Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="33a67-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="33a67-105">Bei einem Beispiel und einem sequenziellen Klassifizierer schätzt die Klassifizierungs Wahrscheinlichkeit für dieses Beispiel, indem die Ausgabe des Klassifizierers für das jeweilige Beispiel wiederholt gemessen wird.</span><span class="sxs-lookup"><span data-stu-id="33a67-105">Given a sample and a sequential classifier, estimates the classification probability for that sample by repeatedly measuring the output of the classifier on the given sample.</span></span>

```qsharp
operation EstimateClassificationProbability (tolerance : Double, model : Microsoft.Quantum.MachineLearning.SequentialModel, sample : Double[], nMeasurements : Int) : Double
```


## <a name="input"></a><span data-ttu-id="33a67-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="33a67-106">Input</span></span>

### <a name="tolerance--double"></a><span data-ttu-id="33a67-107">Toleranz: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="33a67-107">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="33a67-108">Die Toleranz, die das Codieren des Beispiels in einen Zustands Vorbereitungs Vorgang zulässt.</span><span class="sxs-lookup"><span data-stu-id="33a67-108">The tolerance to allow in encoding the sample into a state preparation operation.</span></span>


### <a name="model--sequentialmodel"></a><span data-ttu-id="33a67-109">Modell: [sequentialmodel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="33a67-109">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>

<span data-ttu-id="33a67-110">Das sequenzielle Modell, das zum Schätzen der Klassifizierungs Wahrscheinlichkeit für das angegebene Beispiel verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="33a67-110">The sequential model to be used to estimate the classification probability for the given sample.</span></span>


### <a name="sample--double"></a><span data-ttu-id="33a67-111">Beispiel: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="33a67-111">sample : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="33a67-112">Der Funktions Vektor für das zu klassifizierende Beispiel.</span><span class="sxs-lookup"><span data-stu-id="33a67-112">The feature vector for the sample to be classified.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="33a67-113">nmessungen: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="33a67-113">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="33a67-114">Die Anzahl der Messungen, die beim Schätzen der Klassifizierungs Wahrscheinlichkeit verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="33a67-114">The number of measurements to use in estimating the classification probability.</span></span>



## <a name="output--double"></a><span data-ttu-id="33a67-115">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="33a67-115">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="33a67-116">Eine Schätzung der Klassifizierungs Wahrscheinlichkeit für das angegebene Beispiel.</span><span class="sxs-lookup"><span data-stu-id="33a67-116">An estimate of the classification probability for the given sample.</span></span>
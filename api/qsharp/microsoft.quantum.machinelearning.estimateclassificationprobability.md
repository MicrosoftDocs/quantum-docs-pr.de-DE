---
uid: Microsoft.Quantum.MachineLearning.EstimateClassificationProbability
title: Estimateclassificationwahrscheinlichkeits-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: EstimateClassificationProbability
qsharp.summary: Given a sample and a sequential classifier, estimates the classification probability for that sample by repeatedly measuring the output of the classifier on the given sample.
ms.openlocfilehash: 79e40bc4bc0954dc6742307122609950bf22ec71
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701382"
---
# <a name="estimateclassificationprobability-operation"></a><span data-ttu-id="747e9-102">Estimateclassificationwahrscheinlichkeits-Vorgang</span><span class="sxs-lookup"><span data-stu-id="747e9-102">EstimateClassificationProbability operation</span></span>

<span data-ttu-id="747e9-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="747e9-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="747e9-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="747e9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="747e9-105">Bei einem Beispiel und einem sequenziellen Klassifizierer schätzt die Klassifizierungs Wahrscheinlichkeit für dieses Beispiel, indem die Ausgabe des Klassifizierers für das jeweilige Beispiel wiederholt gemessen wird.</span><span class="sxs-lookup"><span data-stu-id="747e9-105">Given a sample and a sequential classifier, estimates the classification probability for that sample by repeatedly measuring the output of the classifier on the given sample.</span></span>

```qsharp
operation EstimateClassificationProbability (tolerance : Double, model : Microsoft.Quantum.MachineLearning.SequentialModel, sample : Double[], nMeasurements : Int) : Double
```


## <a name="input"></a><span data-ttu-id="747e9-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="747e9-106">Input</span></span>

### <a name="tolerance--double"></a><span data-ttu-id="747e9-107">Toleranz: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="747e9-107">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="747e9-108">Die Toleranz, die das Codieren des Beispiels in einen Zustands Vorbereitungs Vorgang zulässt.</span><span class="sxs-lookup"><span data-stu-id="747e9-108">The tolerance to allow in encoding the sample into a state preparation operation.</span></span>


### <a name="model--sequentialmodel"></a><span data-ttu-id="747e9-109">Modell: [sequentialmodel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="747e9-109">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>

<span data-ttu-id="747e9-110">Das sequenzielle Modell, das zum Schätzen der Klassifizierungs Wahrscheinlichkeit für das angegebene Beispiel verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="747e9-110">The sequential model to be used to estimate the classification probability for the given sample.</span></span>


### <a name="sample--double"></a><span data-ttu-id="747e9-111">Beispiel: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="747e9-111">sample : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="747e9-112">Der Funktions Vektor für das zu klassifizierende Beispiel.</span><span class="sxs-lookup"><span data-stu-id="747e9-112">The feature vector for the sample to be classified.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="747e9-113">nmessungen: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="747e9-113">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="747e9-114">Die Anzahl der Messungen, die beim Schätzen der Klassifizierungs Wahrscheinlichkeit verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="747e9-114">The number of measurements to use in estimating the classification probability.</span></span>



## <a name="output--double"></a><span data-ttu-id="747e9-115">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="747e9-115">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="747e9-116">Eine Schätzung der Klassifizierungs Wahrscheinlichkeit für das angegebene Beispiel.</span><span class="sxs-lookup"><span data-stu-id="747e9-116">An estimate of the classification probability for the given sample.</span></span>
---
uid: Microsoft.Quantum.MachineLearning._RunSingleTrainingEpoch
title: _RunSingleTrainingEpoch Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: _RunSingleTrainingEpoch
qsharp.summary: Perform one epoch of sequential classifier training on a subset of data samples.
ms.openlocfilehash: 71780645a025972f11f32f8ba8fd94d098604f9e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196751"
---
# <a name="_runsingletrainingepoch-operation"></a><span data-ttu-id="58ef3-102">_RunSingleTrainingEpoch Vorgang</span><span class="sxs-lookup"><span data-stu-id="58ef3-102">_RunSingleTrainingEpoch operation</span></span>

<span data-ttu-id="58ef3-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="58ef3-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="58ef3-104">Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="58ef3-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="58ef3-105">Führen Sie eine Epoche sequenzieller Klassifizierungs Schulungen für eine Teilmenge von Daten Beispielen aus.</span><span class="sxs-lookup"><span data-stu-id="58ef3-105">Perform one epoch of sequential classifier training on a subset of data samples.</span></span>

```qsharp
operation _RunSingleTrainingEpoch (encodedSamples : (Microsoft.Quantum.MachineLearning.LabeledSample, Microsoft.Quantum.MachineLearning.StateGenerator)[], schedule : Microsoft.Quantum.MachineLearning.SamplingSchedule, periodScore : Int, options : Microsoft.Quantum.MachineLearning.TrainingOptions, model : Microsoft.Quantum.MachineLearning.SequentialModel, nPreviousBestMisses : Int) : (Int, Microsoft.Quantum.MachineLearning.SequentialModel)
```


## <a name="input"></a><span data-ttu-id="58ef3-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="58ef3-106">Input</span></span>

### <a name="encodedsamples--labeledsamplestategenerator"></a><span data-ttu-id="58ef3-107">encodsamples: ([labeledsample](xref:Microsoft.Quantum.MachineLearning.LabeledSample),[stategenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)) []</span><span class="sxs-lookup"><span data-stu-id="58ef3-107">encodedSamples : ([LabeledSample](xref:Microsoft.Quantum.MachineLearning.LabeledSample),[StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator))[]</span></span>




### <a name="schedule--samplingschedule"></a><span data-ttu-id="58ef3-108">Zeitplan: [samplingschedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span><span class="sxs-lookup"><span data-stu-id="58ef3-108">schedule : [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span></span>




### <a name="periodscore--int"></a><span data-ttu-id="58ef3-109">periodscore: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="58ef3-109">periodScore : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="58ef3-110">Die Anzahl der Verlaufs Schritte, die zwischen Bewertungs Punkten durchgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="58ef3-110">The number of gradient steps to be taken between scoring points.</span></span>
<span data-ttu-id="58ef3-111">Legen Sie für optimale Genauigkeit den Wert 1 fest.</span><span class="sxs-lookup"><span data-stu-id="58ef3-111">For best accuracy, set to 1.</span></span>


### <a name="options--trainingoptions"></a><span data-ttu-id="58ef3-112">Optionen: [trainingoptions](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)</span><span class="sxs-lookup"><span data-stu-id="58ef3-112">options : [TrainingOptions](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)</span></span>

<span data-ttu-id="58ef3-113">Optionen, die beim Training verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="58ef3-113">Options to be used in training.</span></span>


### <a name="model--sequentialmodel"></a><span data-ttu-id="58ef3-114">Modell: [sequentialmodel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="58ef3-114">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>

<span data-ttu-id="58ef3-115">Das sequenzielle Modell, das trainiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="58ef3-115">The sequential model to be trained.</span></span>


### <a name="npreviousbestmisses--int"></a><span data-ttu-id="58ef3-116">npreviousbestmissen: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="58ef3-116">nPreviousBestMisses : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="58ef3-117">Die beste Anzahl von fehl Klassifizierungen, die in früheren Epochen beobachtet wurden.</span><span class="sxs-lookup"><span data-stu-id="58ef3-117">The best number of misclassifications observed in previous epochs.</span></span>



## <a name="output--intsequentialmodel"></a><span data-ttu-id="58ef3-118">Ausgabe: ([int](xref:microsoft.quantum.lang-ref.int),[sequentialmodel](xref:Microsoft.Quantum.MachineLearning.SequentialModel))</span><span class="sxs-lookup"><span data-stu-id="58ef3-118">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel))</span></span>

- <span data-ttu-id="58ef3-119">Die kleinste Anzahl von fehl Klassifizierungen, die bis zu dieser Epoche beobachtet wurden.</span><span class="sxs-lookup"><span data-stu-id="58ef3-119">The smallest number of misclassifications observed through to this epoch.</span></span>
- <span data-ttu-id="58ef3-120">Das neue beste sequenzielle Modell, das gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="58ef3-120">The new best sequential model found.</span></span>
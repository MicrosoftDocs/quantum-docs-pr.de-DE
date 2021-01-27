---
uid: Microsoft.Quantum.MachineLearning.TrainSequentialClassifierAtModel
title: Trainsequentialclassifieratmodel-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: TrainSequentialClassifierAtModel
qsharp.summary: Given the structure of a sequential classifier, trains the classifier on a given labeled training set, starting from a particular model.
ms.openlocfilehash: 4164c190cb19b6d3ea74d9803a77d2b19607279b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857157"
---
# <a name="trainsequentialclassifieratmodel-operation"></a><span data-ttu-id="bacd2-102">Trainsequentialclassifieratmodel-Vorgang</span><span class="sxs-lookup"><span data-stu-id="bacd2-102">TrainSequentialClassifierAtModel operation</span></span>

<span data-ttu-id="bacd2-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="bacd2-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="bacd2-104">Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="bacd2-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="bacd2-105">Trainiert bei der Struktur eines sequenziellen Klassifizierers den Klassifizierer für einen angegebenen beschrifteten Trainings Satz, beginnend mit einem bestimmten Modell.</span><span class="sxs-lookup"><span data-stu-id="bacd2-105">Given the structure of a sequential classifier, trains the classifier on a given labeled training set, starting from a particular model.</span></span>

```qsharp
operation TrainSequentialClassifierAtModel (model : Microsoft.Quantum.MachineLearning.SequentialModel, samples : Microsoft.Quantum.MachineLearning.LabeledSample[], options : Microsoft.Quantum.MachineLearning.TrainingOptions, trainingSchedule : Microsoft.Quantum.MachineLearning.SamplingSchedule, validationSchedule : Microsoft.Quantum.MachineLearning.SamplingSchedule) : (Microsoft.Quantum.MachineLearning.SequentialModel, Int)
```


## <a name="input"></a><span data-ttu-id="bacd2-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bacd2-106">Input</span></span>

### <a name="model--sequentialmodel"></a><span data-ttu-id="bacd2-107">Modell: [sequentialmodel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="bacd2-107">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>

<span data-ttu-id="bacd2-108">Das sequenzielle Modell, das als Ausgangspunkt für das Training verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="bacd2-108">The sequential model to be used as a starting point for training.</span></span>


### <a name="samples--labeledsample"></a><span data-ttu-id="bacd2-109">Beispiele: [labeledsample](xref:Microsoft.Quantum.MachineLearning.LabeledSample)[]</span><span class="sxs-lookup"><span data-stu-id="bacd2-109">samples : [LabeledSample](xref:Microsoft.Quantum.MachineLearning.LabeledSample)[]</span></span>

<span data-ttu-id="bacd2-110">Eine Reihe von beschrifteten Trainingsdaten, die zum Durchführen von Schulungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bacd2-110">A set of labeled training data that will be used to perform training.</span></span>


### <a name="options--trainingoptions"></a><span data-ttu-id="bacd2-111">Optionen: [trainingoptions](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)</span><span class="sxs-lookup"><span data-stu-id="bacd2-111">options : [TrainingOptions](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)</span></span>

<span data-ttu-id="bacd2-112">Konfiguration, die beim Training verwendet werden soll. Weitere Informationen finden Sie unter @"microsoft.quantum.machinelearning.trainingoptions" und @"microsoft.quantum.machinelearning.defaulttrainingoptions" .</span><span class="sxs-lookup"><span data-stu-id="bacd2-112">Configuration to be used when training; see @"microsoft.quantum.machinelearning.trainingoptions" and @"microsoft.quantum.machinelearning.defaulttrainingoptions" for more details.</span></span>


### <a name="trainingschedule--samplingschedule"></a><span data-ttu-id="bacd2-113">trainingschedule: [samplingschedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span><span class="sxs-lookup"><span data-stu-id="bacd2-113">trainingSchedule : [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span></span>

<span data-ttu-id="bacd2-114">Ein Stichproben Zeitplan, der beim Auswählen von Beispielen aus den Trainingsdaten während der Trainingsschritte verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="bacd2-114">A sampling schedule to use when selecting samples from the training data during training steps.</span></span>


### <a name="validationschedule--samplingschedule"></a><span data-ttu-id="bacd2-115">validationschedule: [samplingschedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span><span class="sxs-lookup"><span data-stu-id="bacd2-115">validationSchedule : [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span></span>

<span data-ttu-id="bacd2-116">Ein Stichproben Zeitplan, der beim Auswählen von Beispielen aus den Trainingsdaten verwendet werden soll, wenn ausgewählt wird, welcher Startpunkt zu dem besten Klassifizierungs Ergebnis geführt hat.</span><span class="sxs-lookup"><span data-stu-id="bacd2-116">A sampling schedule to use when selecting samples from the training data when selecting which start point resulted in the best classifier score.</span></span>



## <a name="output--sequentialmodelint"></a><span data-ttu-id="bacd2-117">Ausgabe: ([sequentialmodel](xref:Microsoft.Quantum.MachineLearning.SequentialModel),[int](xref:microsoft.quantum.lang-ref.int))</span><span class="sxs-lookup"><span data-stu-id="bacd2-117">Output : ([SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel),[Int](xref:microsoft.quantum.lang-ref.int))</span></span>

- <span data-ttu-id="bacd2-118">Eine Parametrisierung des angegebenen Klassifizierers und eine Abweichung zwischen den beiden Klassen, die dem besten Ergebnis aus den einzelnen angegebenen Startpunkten entspricht.</span><span class="sxs-lookup"><span data-stu-id="bacd2-118">A parameterization of the given classifier and a bias between the two classes, together corresponding to the best result from each of the given start points.</span></span>
- <span data-ttu-id="bacd2-119">Die Anzahl der im besten Klassifizierungs Modell beobachteten Fehler.</span><span class="sxs-lookup"><span data-stu-id="bacd2-119">The number of misses observed at the best classifier model.</span></span>

## <a name="see-also"></a><span data-ttu-id="bacd2-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="bacd2-120">See Also</span></span>

- [<span data-ttu-id="bacd2-121">Microsoft. Quantum. machinelearning. trainsequentialclassifier</span><span class="sxs-lookup"><span data-stu-id="bacd2-121">Microsoft.Quantum.MachineLearning.TrainSequentialClassifier</span></span>](xref:Microsoft.Quantum.MachineLearning.TrainSequentialClassifier)
- [<span data-ttu-id="bacd2-122">Microsoft. Quantum. machinelearning. validatesequentialclassifier</span><span class="sxs-lookup"><span data-stu-id="bacd2-122">Microsoft.Quantum.MachineLearning.ValidateSequentialClassifier</span></span>](xref:Microsoft.Quantum.MachineLearning.ValidateSequentialClassifier)
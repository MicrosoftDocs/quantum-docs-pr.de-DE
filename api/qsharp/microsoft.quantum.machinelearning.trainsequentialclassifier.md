---
uid: Microsoft.Quantum.MachineLearning.TrainSequentialClassifier
title: Trainsequentialclassifier-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: TrainSequentialClassifier
qsharp.summary: Given the structure of a sequential classifier, trains the classifier on a given labeled training set.
ms.openlocfilehash: d0b0587ffa93141739bcd6f39324571ffc28dacc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96228660"
---
# <a name="trainsequentialclassifier-operation"></a><span data-ttu-id="eaaf0-102">Trainsequentialclassifier-Vorgang</span><span class="sxs-lookup"><span data-stu-id="eaaf0-102">TrainSequentialClassifier operation</span></span>

<span data-ttu-id="eaaf0-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="eaaf0-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="eaaf0-104">Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="eaaf0-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="eaaf0-105">Trainiert bei der Struktur eines sequenziellen Klassifizierers den Klassifizierer für einen angegebenen beschrifteten Trainings Satz.</span><span class="sxs-lookup"><span data-stu-id="eaaf0-105">Given the structure of a sequential classifier, trains the classifier on a given labeled training set.</span></span>

```qsharp
operation TrainSequentialClassifier (models : Microsoft.Quantum.MachineLearning.SequentialModel[], samples : Microsoft.Quantum.MachineLearning.LabeledSample[], options : Microsoft.Quantum.MachineLearning.TrainingOptions, trainingSchedule : Microsoft.Quantum.MachineLearning.SamplingSchedule, validationSchedule : Microsoft.Quantum.MachineLearning.SamplingSchedule) : (Microsoft.Quantum.MachineLearning.SequentialModel, Int)
```


## <a name="input"></a><span data-ttu-id="eaaf0-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="eaaf0-106">Input</span></span>

### <a name="models--sequentialmodel"></a><span data-ttu-id="eaaf0-107">Modelle: [sequentialmodel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)[]</span><span class="sxs-lookup"><span data-stu-id="eaaf0-107">models : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)[]</span></span>

<span data-ttu-id="eaaf0-108">Ein Array von Modellen, die während des Trainings als Ausgangspunkt verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="eaaf0-108">An array of models to be used as starting points during training.</span></span>


### <a name="samples--labeledsample"></a><span data-ttu-id="eaaf0-109">Beispiele: [labeledsample](xref:Microsoft.Quantum.MachineLearning.LabeledSample)[]</span><span class="sxs-lookup"><span data-stu-id="eaaf0-109">samples : [LabeledSample](xref:Microsoft.Quantum.MachineLearning.LabeledSample)[]</span></span>

<span data-ttu-id="eaaf0-110">Eine Reihe von beschrifteten Trainingsdaten, die zum Durchführen von Schulungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eaaf0-110">A set of labeled training data that will be used to perform training.</span></span>


### <a name="options--trainingoptions"></a><span data-ttu-id="eaaf0-111">Optionen: [trainingoptions](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)</span><span class="sxs-lookup"><span data-stu-id="eaaf0-111">options : [TrainingOptions](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)</span></span>

<span data-ttu-id="eaaf0-112">Konfiguration, die beim Training verwendet werden soll. Weitere Informationen finden Sie unter @"microsoft.quantum.machinelearning.trainingoptions" und @"microsoft.quantum.machinelearning.defaulttrainingoptions" .</span><span class="sxs-lookup"><span data-stu-id="eaaf0-112">Configuration to be used when training; see @"microsoft.quantum.machinelearning.trainingoptions" and @"microsoft.quantum.machinelearning.defaulttrainingoptions" for more details.</span></span>


### <a name="trainingschedule--samplingschedule"></a><span data-ttu-id="eaaf0-113">trainingschedule: [samplingschedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span><span class="sxs-lookup"><span data-stu-id="eaaf0-113">trainingSchedule : [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span></span>

<span data-ttu-id="eaaf0-114">Ein Stichproben Zeitplan, der beim Auswählen von Beispielen aus den Trainingsdaten während der Trainingsschritte verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="eaaf0-114">A sampling schedule to use when selecting samples from the training data during training steps.</span></span>


### <a name="validationschedule--samplingschedule"></a><span data-ttu-id="eaaf0-115">validationschedule: [samplingschedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span><span class="sxs-lookup"><span data-stu-id="eaaf0-115">validationSchedule : [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span></span>

<span data-ttu-id="eaaf0-116">Ein Stichproben Zeitplan, der beim Auswählen von Beispielen aus den Trainingsdaten verwendet werden soll, wenn ausgewählt wird, welcher Startpunkt zu dem besten Klassifizierungs Ergebnis geführt hat.</span><span class="sxs-lookup"><span data-stu-id="eaaf0-116">A sampling schedule to use when selecting samples from the training data when selecting which start point resulted in the best classifier score.</span></span>



## <a name="output--sequentialmodelint"></a><span data-ttu-id="eaaf0-117">Ausgabe: ([sequentialmodel](xref:Microsoft.Quantum.MachineLearning.SequentialModel),[int](xref:microsoft.quantum.lang-ref.int))</span><span class="sxs-lookup"><span data-stu-id="eaaf0-117">Output : ([SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel),[Int](xref:microsoft.quantum.lang-ref.int))</span></span>

- <span data-ttu-id="eaaf0-118">Eine Parametrisierung des angegebenen Klassifizierers und eine Abweichung zwischen den beiden Klassen, die dem besten Ergebnis aus den einzelnen angegebenen Startpunkten entspricht.</span><span class="sxs-lookup"><span data-stu-id="eaaf0-118">A parameterization of the given classifier and a bias between the two classes, together corresponding to the best result from each of the given start points.</span></span>
- <span data-ttu-id="eaaf0-119">Die Anzahl der im besten Klassifizierungs Modell beobachteten Fehler.</span><span class="sxs-lookup"><span data-stu-id="eaaf0-119">The number of misses observed at the best classifier model.</span></span>

## <a name="see-also"></a><span data-ttu-id="eaaf0-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="eaaf0-120">See Also</span></span>

- [<span data-ttu-id="eaaf0-121">Microsoft. Quantum. machinelearning. trainsequentialclassifieratmodel</span><span class="sxs-lookup"><span data-stu-id="eaaf0-121">Microsoft.Quantum.MachineLearning.TrainSequentialClassifierAtModel</span></span>](xref:Microsoft.Quantum.MachineLearning.TrainSequentialClassifierAtModel)
- [<span data-ttu-id="eaaf0-122">Microsoft. Quantum. machinelearning. validatesequentialclassifier</span><span class="sxs-lookup"><span data-stu-id="eaaf0-122">Microsoft.Quantum.MachineLearning.ValidateSequentialClassifier</span></span>](xref:Microsoft.Quantum.MachineLearning.ValidateSequentialClassifier)
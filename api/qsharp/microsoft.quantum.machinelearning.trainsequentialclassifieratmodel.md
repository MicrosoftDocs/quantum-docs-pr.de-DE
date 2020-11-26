---
uid: Microsoft.Quantum.MachineLearning.TrainSequentialClassifierAtModel
title: Trainsequentialclassifieratmodel-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: TrainSequentialClassifierAtModel
qsharp.summary: Given the structure of a sequential classifier, trains the classifier on a given labeled training set, starting from a particular model.
ms.openlocfilehash: 02a300a2e1029d0e09aba19d090e15128fede717
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211462"
---
# <a name="trainsequentialclassifieratmodel-operation"></a>Trainsequentialclassifieratmodel-Vorgang

Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)

Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Trainiert bei der Struktur eines sequenziellen Klassifizierers den Klassifizierer für einen angegebenen beschrifteten Trainings Satz, beginnend mit einem bestimmten Modell.

```qsharp
operation TrainSequentialClassifierAtModel (model : Microsoft.Quantum.MachineLearning.SequentialModel, samples : Microsoft.Quantum.MachineLearning.LabeledSample[], options : Microsoft.Quantum.MachineLearning.TrainingOptions, trainingSchedule : Microsoft.Quantum.MachineLearning.SamplingSchedule, validationSchedule : Microsoft.Quantum.MachineLearning.SamplingSchedule) : (Microsoft.Quantum.MachineLearning.SequentialModel, Int)
```


## <a name="input"></a>Eingabe

### <a name="model--sequentialmodel"></a>Modell: [sequentialmodel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)

Das sequenzielle Modell, das als Ausgangspunkt für das Training verwendet werden soll.


### <a name="samples--labeledsample"></a>Beispiele: [labeledsample](xref:Microsoft.Quantum.MachineLearning.LabeledSample)[]

Eine Reihe von beschrifteten Trainingsdaten, die zum Durchführen von Schulungen verwendet werden.


### <a name="options--trainingoptions"></a>Optionen: [trainingoptions](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)

Konfiguration, die beim Training verwendet werden soll. Weitere Informationen finden Sie unter @"microsoft.quantum.machinelearning.trainingoptions" und @"microsoft.quantum.machinelearning.defaulttrainingoptions" .


### <a name="trainingschedule--samplingschedule"></a>trainingschedule: [samplingschedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)

Ein Stichproben Zeitplan, der beim Auswählen von Beispielen aus den Trainingsdaten während der Trainingsschritte verwendet werden soll.


### <a name="validationschedule--samplingschedule"></a>validationschedule: [samplingschedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)

Ein Stichproben Zeitplan, der beim Auswählen von Beispielen aus den Trainingsdaten verwendet werden soll, wenn ausgewählt wird, welcher Startpunkt zu dem besten Klassifizierungs Ergebnis geführt hat.



## <a name="output--sequentialmodelint"></a>Ausgabe: ([sequentialmodel](xref:Microsoft.Quantum.MachineLearning.SequentialModel),[int](xref:microsoft.quantum.lang-ref.int))

- Eine Parametrisierung des angegebenen Klassifizierers und eine Abweichung zwischen den beiden Klassen, die dem besten Ergebnis aus den einzelnen angegebenen Startpunkten entspricht.
- Die Anzahl der im besten Klassifizierungs Modell beobachteten Fehler.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. machinelearning. trainsequentialclassifier](xref:Microsoft.Quantum.MachineLearning.TrainSequentialClassifier)
- [Microsoft. Quantum. machinelearning. validatesequentialclassifier](xref:Microsoft.Quantum.MachineLearning.ValidateSequentialClassifier)
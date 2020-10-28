---
uid: Microsoft.Quantum.MachineLearning.TrainSequentialClassifier
title: Trainsequentialclassifier-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: TrainSequentialClassifier
qsharp.summary: Given the structure of a sequential classifier, trains the classifier on a given labeled training set.
ms.openlocfilehash: 12c4df59941b682d9de798e6585b59d1c34924dc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702041"
---
# <a name="trainsequentialclassifier-operation"></a>Trainsequentialclassifier-Vorgang

Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)

Paketen [](https://nuget.org/packages/)


Trainiert bei der Struktur eines sequenziellen Klassifizierers den Klassifizierer für einen angegebenen beschrifteten Trainings Satz.

```qsharp
operation TrainSequentialClassifier (models : Microsoft.Quantum.MachineLearning.SequentialModel[], samples : Microsoft.Quantum.MachineLearning.LabeledSample[], options : Microsoft.Quantum.MachineLearning.TrainingOptions, trainingSchedule : Microsoft.Quantum.MachineLearning.SamplingSchedule, validationSchedule : Microsoft.Quantum.MachineLearning.SamplingSchedule) : (Microsoft.Quantum.MachineLearning.SequentialModel, Int)
```


## <a name="input"></a>Eingabe

### <a name="models--sequentialmodel"></a>Modelle: [sequentialmodel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)[]

Ein Array von Modellen, die während des Trainings als Ausgangspunkt verwendet werden sollen.


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

- [Microsoft. Quantum. machinelearning. trainsequentialclassifieratmodel](xref:Microsoft.Quantum.MachineLearning.TrainSequentialClassifierAtModel)
- [Microsoft. Quantum. machinelearning. validatesequentialclassifier](xref:Microsoft.Quantum.MachineLearning.ValidateSequentialClassifier)
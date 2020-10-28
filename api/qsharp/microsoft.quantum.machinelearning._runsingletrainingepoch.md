---
uid: Microsoft.Quantum.MachineLearning._RunSingleTrainingEpoch
title: _RunSingleTrainingEpoch Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: _RunSingleTrainingEpoch
qsharp.summary: Perform one epoch of sequential classifier training on a subset of data samples.
ms.openlocfilehash: 2b4f629eac0bd8e60bd4d86077521c60085d4809
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706951"
---
# <a name="_runsingletrainingepoch-operation"></a>_RunSingleTrainingEpoch Vorgang

Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)

Paketen [](https://nuget.org/packages/)


Führen Sie eine Epoche sequenzieller Klassifizierungs Schulungen für eine Teilmenge von Daten Beispielen aus.

```qsharp
operation _RunSingleTrainingEpoch (encodedSamples : (Microsoft.Quantum.MachineLearning.LabeledSample, Microsoft.Quantum.MachineLearning.StateGenerator)[], schedule : Microsoft.Quantum.MachineLearning.SamplingSchedule, periodScore : Int, options : Microsoft.Quantum.MachineLearning.TrainingOptions, model : Microsoft.Quantum.MachineLearning.SequentialModel, nPreviousBestMisses : Int) : (Int, Microsoft.Quantum.MachineLearning.SequentialModel)
```


## <a name="input"></a>Eingabe

### <a name="encodedsamples--labeledsamplestategenerator"></a>encodsamples: ([labeledsample](xref:Microsoft.Quantum.MachineLearning.LabeledSample),[stategenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)) []




### <a name="schedule--samplingschedule"></a>Zeitplan: [samplingschedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)




### <a name="periodscore--int"></a>periodscore: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der Verlaufs Schritte, die zwischen Bewertungs Punkten durchgeführt werden sollen.
Legen Sie für optimale Genauigkeit den Wert 1 fest.


### <a name="options--trainingoptions"></a>Optionen: [trainingoptions](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)

Optionen, die beim Training verwendet werden sollen.


### <a name="model--sequentialmodel"></a>Modell: [sequentialmodel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)

Das sequenzielle Modell, das trainiert werden soll.


### <a name="npreviousbestmisses--int"></a>npreviousbestmissen: [int](xref:microsoft.quantum.lang-ref.int)

Die beste Anzahl von fehl Klassifizierungen, die in früheren Epochen beobachtet wurden.



## <a name="output--intsequentialmodel"></a>Ausgabe: ([int](xref:microsoft.quantum.lang-ref.int),[sequentialmodel](xref:Microsoft.Quantum.MachineLearning.SequentialModel))

- Die kleinste Anzahl von fehl Klassifizierungen, die bis zu dieser Epoche beobachtet wurden.
- Das neue beste sequenzielle Modell, das gefunden wurde.
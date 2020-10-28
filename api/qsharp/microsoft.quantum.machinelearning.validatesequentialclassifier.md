---
uid: Microsoft.Quantum.MachineLearning.ValidateSequentialClassifier
title: Validatesequentialclassifier-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ValidateSequentialClassifier
qsharp.summary: Validates a given sequential classifier against a given set of pre-labeled samples.
ms.openlocfilehash: 802f1045ea4086bd371d68018a481182cb75b209
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706826"
---
# <a name="validatesequentialclassifier-operation"></a>Validatesequentialclassifier-Vorgang

Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)

Paketen [](https://nuget.org/packages/)


Überprüft einen angegebenen sequenziellen Klassifizierer anhand eines angegebenen Satzes von vorbeschrifteten Beispielen.

```qsharp
operation ValidateSequentialClassifier (model : Microsoft.Quantum.MachineLearning.SequentialModel, samples : Microsoft.Quantum.MachineLearning.LabeledSample[], tolerance : Double, nMeasurements : Int, validationSchedule : Microsoft.Quantum.MachineLearning.SamplingSchedule) : Microsoft.Quantum.MachineLearning.ValidationResults
```


## <a name="input"></a>Eingabe

### <a name="model--sequentialmodel"></a>Modell: [sequentialmodel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)

Das sequenzielle Modell, das überprüft werden soll.


### <a name="samples--labeledsample"></a>Beispiele: [labeledsample](xref:Microsoft.Quantum.MachineLearning.LabeledSample)[]

Die Beispiele, die zum Überprüfen des angegebenen Modells verwendet werden sollen.


### <a name="tolerance--double"></a>Toleranz: [Double](xref:microsoft.quantum.lang-ref.double)

Die Näherungs Toleranz, die beim Codieren der einzelnen Stichproben als Eingabe für den sequenziellen Klassifizierer verwendet wird.


### <a name="nmeasurements--int"></a>nmessungen: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der für die Klassifizierung der einzelnen Stichproben zu verwendenden Messungen.


### <a name="validationschedule--samplingschedule"></a>validationschedule: [samplingschedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)

Der Zeitplan, nach dem Beispiele aus dem Validierungs Satz gezeichnet werden sollen.



## <a name="output--validationresults"></a>Ausgabe: [ValidationResults](xref:Microsoft.Quantum.MachineLearning.ValidationResults)

Die Ergebnisse der angegebenen Validierung.
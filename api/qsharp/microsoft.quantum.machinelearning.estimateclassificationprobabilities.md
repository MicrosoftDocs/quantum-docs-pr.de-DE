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
# <a name="estimateclassificationprobabilities-operation"></a>Estimateclassificationprobabiliesoperation

Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)

Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Bei einer Reihe von Beispielen und einem sequenziellen Klassifizierer wird die Klassifizierungs Wahrscheinlichkeit für diese Stichproben durch wiederholtes Messen der Ausgabe des Klassifizierers in den einzelnen Stichproben geschätzt.

```qsharp
operation EstimateClassificationProbabilities (tolerance : Double, model : Microsoft.Quantum.MachineLearning.SequentialModel, samples : Double[][], nMeasurements : Int) : Double[]
```


## <a name="input"></a>Eingabe

### <a name="tolerance--double"></a>Toleranz: [Double](xref:microsoft.quantum.lang-ref.double)

Die Toleranz, die das Codieren des Beispiels in einen Zustands Vorbereitungs Vorgang zulässt.


### <a name="model--sequentialmodel"></a>Modell: [sequentialmodel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)

Das sequenzielle Modell, das zum Schätzen der Klassifizierungs Wahrscheinlichkeiten für die angegebenen Beispiele verwendet werden soll.


### <a name="samples--double"></a>Beispiele: [Double](xref:microsoft.quantum.lang-ref.double)[] []

Ein Array von Merkmals Vektoren für jede zu klassifizierende Stichprobe.


### <a name="nmeasurements--int"></a>nmessungen: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der Messungen, die beim Schätzen der Klassifizierungs Wahrscheinlichkeit verwendet werden sollen.



## <a name="output--double"></a>Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)[]

Ein Array von Schätzungen der Klassifizierungs Wahrscheinlichkeit für jedes gegebene Beispiel.
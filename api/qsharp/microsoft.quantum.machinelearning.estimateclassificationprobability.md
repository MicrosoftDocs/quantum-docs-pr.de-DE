---
uid: Microsoft.Quantum.MachineLearning.EstimateClassificationProbability
title: Estimateclassificationwahrscheinlichkeits-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: EstimateClassificationProbability
qsharp.summary: Given a sample and a sequential classifier, estimates the classification probability for that sample by repeatedly measuring the output of the classifier on the given sample.
ms.openlocfilehash: c2b74bc55ad9005a8f52d05796e856f4f2fb62ba
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853935"
---
# <a name="estimateclassificationprobability-operation"></a>Estimateclassificationwahrscheinlichkeits-Vorgang

Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)

Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Bei einem Beispiel und einem sequenziellen Klassifizierer schätzt die Klassifizierungs Wahrscheinlichkeit für dieses Beispiel, indem die Ausgabe des Klassifizierers für das jeweilige Beispiel wiederholt gemessen wird.

```qsharp
operation EstimateClassificationProbability (tolerance : Double, model : Microsoft.Quantum.MachineLearning.SequentialModel, sample : Double[], nMeasurements : Int) : Double
```


## <a name="input"></a>Eingabe

### <a name="tolerance--double"></a>Toleranz: [Double](xref:microsoft.quantum.lang-ref.double)

Die Toleranz, die das Codieren des Beispiels in einen Zustands Vorbereitungs Vorgang zulässt.


### <a name="model--sequentialmodel"></a>Modell: [sequentialmodel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)

Das sequenzielle Modell, das zum Schätzen der Klassifizierungs Wahrscheinlichkeit für das angegebene Beispiel verwendet werden soll.


### <a name="sample--double"></a>Beispiel: [Double](xref:microsoft.quantum.lang-ref.double)[]

Der Funktions Vektor für das zu klassifizierende Beispiel.


### <a name="nmeasurements--int"></a>nmessungen: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der Messungen, die beim Schätzen der Klassifizierungs Wahrscheinlichkeit verwendet werden sollen.



## <a name="output--double"></a>Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)

Eine Schätzung der Klassifizierungs Wahrscheinlichkeit für das angegebene Beispiel.
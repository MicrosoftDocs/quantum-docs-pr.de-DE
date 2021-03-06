---
uid: Microsoft.Quantum.MachineLearning.EstimateGradient
title: Estimategradient-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: EstimateGradient
qsharp.summary: Estimates the training gradient for a sequential classifier at a particular model and for a given encoded input.
ms.openlocfilehash: 38edcb67e7dcc5d2e971fb507a792937774a702c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844387"
---
# <a name="estimategradient-operation"></a>Estimategradient-Vorgang

Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)

Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Schätzt den Trainingsverlauf für einen sequenziellen Klassifizierer bei einem bestimmten Modell und für eine bestimmte codierte Eingabe.

```qsharp
operation EstimateGradient (model : Microsoft.Quantum.MachineLearning.SequentialModel, encodedInput : Microsoft.Quantum.MachineLearning.StateGenerator, nMeasurements : Int) : Double[]
```


## <a name="input"></a>Eingabe

### <a name="model--sequentialmodel"></a>Modell: [sequentialmodel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)

Das sequenzielle Modell, dessen Farbverlauf geschätzt wird.


### <a name="encodedinput--stategenerator"></a>encodebug: [stategenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)

Eine Eingabe für den sequenziellen Klassifizierer, die in einen Zustands Vorbereitungs Vorgang codiert ist.


### <a name="nmeasurements--int"></a>nmessungen: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der Messungen, die beim Schätzen des Farbverlaufs verwendet werden sollen.



## <a name="output--double"></a>Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)[]

Eine Schätzung des Trainings Farbverlaufs bei den angegebenen Eingabe-und Modellparametern.

## <a name="remarks"></a>Bemerkungen

Bei diesem Vorgang wird ein Hadamard-Test und die Parameter Verschiebungs Technik verwendet, um den Farbverlauf zu schätzen.
---
uid: Microsoft.Quantum.MachineLearning._RunSingleTrainingStep
title: _RunSingleTrainingStep Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: _RunSingleTrainingStep
qsharp.summary: attempts a single parameter update in the direction of mini batch gradient
ms.openlocfilehash: 3a3fa1ae34bbcc046f3b3cef4c13c0a84c7cc2b4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853960"
---
# <a name="_runsingletrainingstep-operation"></a>_RunSingleTrainingStep Vorgang

Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)

Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


versucht, ein einzelnes Parameter Update in die Richtung des Mini Batch Farbverlaufs zu ändern.

```qsharp
operation _RunSingleTrainingStep (miniBatch : (Microsoft.Quantum.MachineLearning.LabeledSample, Microsoft.Quantum.MachineLearning.StateGenerator)[], options : Microsoft.Quantum.MachineLearning.TrainingOptions, model : Microsoft.Quantum.MachineLearning.SequentialModel) : (Double, Microsoft.Quantum.MachineLearning.SequentialModel)
```


## <a name="input"></a>Eingabe

### <a name="minibatch--labeledsamplestategenerator"></a>minibatch: ([labeledsample](xref:Microsoft.Quantum.MachineLearning.LabeledSample),[stategenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)) []

Container mit gekennzeichneten Beispielen im Mini Batch


### <a name="options--trainingoptions"></a>Optionen: [trainingoptions](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)




### <a name="model--sequentialmodel"></a>Modell: [sequentialmodel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)





## <a name="output--doublesequentialmodel"></a>Ausgabe: ([Double](xref:microsoft.quantum.lang-ref.double),[sequentialmodel](xref:Microsoft.Quantum.MachineLearning.SequentialModel))

(Utility, (New) Parameters) Pair
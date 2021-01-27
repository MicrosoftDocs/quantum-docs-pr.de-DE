---
uid: Microsoft.Quantum.MachineLearning.DefaultTrainingOptions
title: Defaulttrainingoptions-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: DefaultTrainingOptions
qsharp.summary: Returns a default set of options for training classifiers.
ms.openlocfilehash: 474683ce5b9ec22bec686fb29d87728afe24d23a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856008"
---
# <a name="defaulttrainingoptions-function"></a>Defaulttrainingoptions-Funktion

Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)

Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Gibt einen Standardsatz von Optionen für Trainings Klassifizierer zurück.

```qsharp
function DefaultTrainingOptions () : Microsoft.Quantum.MachineLearning.TrainingOptions
```


## <a name="output--trainingoptions"></a>Ausgabe: [trainingoptions](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)

Ein angemessener Satz von Standard Schulungs Optionen, die beim Trainieren von Klassifizierungen verwendet werden.

## <a name="example"></a>Beispiel

Verwenden Sie den-Operator, um die Standardoptionen, aber mit zusätzlichen Messungen, zu verwenden `w/` :

```qsharp
let options = DefaultTrainingOptions()
    w/ NMeasurements <- 1000000;
```
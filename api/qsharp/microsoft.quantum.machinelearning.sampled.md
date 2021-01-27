---
uid: Microsoft.Quantum.MachineLearning.Sampled
title: Sampling-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: Sampled
qsharp.summary: Samples a given array, using the given schedule.
ms.openlocfilehash: 5dd599246847718f4f0411715585cb416595db9d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854950"
---
# <a name="sampled-function"></a>Sampling-Funktion

Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)

Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Prüft ein bestimmtes Array unter Verwendung des angegebenen Zeitplans.

```qsharp
function Sampled<'T> (schedule : Microsoft.Quantum.MachineLearning.SamplingSchedule, values : 'T[]) : 'T[]
```


## <a name="input"></a>Eingabe

### <a name="schedule--samplingschedule"></a>Zeitplan: [samplingschedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)

Ein Zeitplan, der in Stichproben Werten verwendet werden soll.


### <a name="values--t"></a>Werte: 't []

Ein Array von Werten, die abgefragt werden sollen.



## <a name="output--t"></a>Ausgabe: 't []

Ein Array von-Elementen aus-Werten, das nach dem angegebenen Zeitplan liegt.

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF


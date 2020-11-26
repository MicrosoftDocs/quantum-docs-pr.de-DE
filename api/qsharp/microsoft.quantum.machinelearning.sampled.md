---
uid: Microsoft.Quantum.MachineLearning.Sampled
title: Sampling-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: Sampled
qsharp.summary: Samples a given array, using the given schedule.
ms.openlocfilehash: ddff72bbed6f20e8e0ceb3bfe3fc50a3da0bd2a9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211626"
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


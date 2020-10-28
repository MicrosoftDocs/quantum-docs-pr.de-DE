---
uid: Microsoft.Quantum.MachineLearning.Sampled
title: Sampling-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: Sampled
qsharp.summary: Samples a given array, using the given schedule.
ms.openlocfilehash: 9f9f91bc50861c5b31a76e28050189d13efda71e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722429"
---
# <a name="sampled-function"></a>Sampling-Funktion

Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)

Paketen [](https://nuget.org/packages/)


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


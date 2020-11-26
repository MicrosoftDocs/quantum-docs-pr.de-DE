---
uid: Microsoft.Quantum.AmplitudeAmplification.StandardReflectionPhases
title: Standardreflectionphasen-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: StandardReflectionPhases
qsharp.summary: Computes partial reflection phases for standard amplitude amplification.
ms.openlocfilehash: 316c8f22a16859ebb439824eda9a5aa02c750b5d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191124"
---
# <a name="standardreflectionphases-function"></a>Standardreflectionphasen-Funktion

Namespace: [Microsoft. Quantum. Verstärkungs Verstärkung](xref:Microsoft.Quantum.AmplitudeAmplification)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Berechnet partielle Reflexionsphasen für die standardmäßige Amplitude-Verstärkung.

```qsharp
function StandardReflectionPhases (nIterations : Int) : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
```


## <a name="input"></a>Eingabe

### <a name="niterations--int"></a>niterationen: [int](xref:microsoft.quantum.lang-ref.int)

Anzahl der Amplitude-Verstärkungs Iterationen, für die partielle Reflexionsphasen generiert werden sollen.



## <a name="output--reflectionphases"></a>Ausgabe: [reflectionphasen](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)

Ein Vorgang, der als Teil Reflektionen angegebene Phasen implementiert.

## <a name="remarks"></a>Bemerkungen

Alle Phasen sind $ \pi $, mit Ausnahme der ersten Reflektion über den Startstatus und der letzten Reflektion über den Ziel Status ($0 $).
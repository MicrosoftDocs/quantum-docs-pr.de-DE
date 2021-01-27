---
uid: Microsoft.Quantum.AmplitudeAmplification.StandardReflectionPhases
title: Standardreflectionphasen-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: StandardReflectionPhases
qsharp.summary: Computes partial reflection phases for standard amplitude amplification.
ms.openlocfilehash: 703b50d0186cd0f4eddb9a29fa3cffb2b746c8d6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843914"
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
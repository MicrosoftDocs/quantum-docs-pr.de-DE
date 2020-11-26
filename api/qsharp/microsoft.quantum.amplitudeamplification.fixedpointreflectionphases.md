---
uid: Microsoft.Quantum.AmplitudeAmplification.FixedPointReflectionPhases
title: Fixedpointreflectionphasen-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: FixedPointReflectionPhases
qsharp.summary: Computes partial reflection phases for fixed-point amplitude amplification.
ms.openlocfilehash: 8cc1073447f5fae87ece38db64dcc312f6208899
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191447"
---
# <a name="fixedpointreflectionphases-function"></a>Fixedpointreflectionphasen-Funktion

Namespace: [Microsoft. Quantum. Verstärkungs Verstärkung](xref:Microsoft.Quantum.AmplitudeAmplification)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Berechnet partielle reflektionsprozesse für die Verstärkung der Amplitude-Amplitude mit fester Breite.

```qsharp
function FixedPointReflectionPhases (nQueries : Int, successMin : Double) : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
```


## <a name="input"></a>Eingabe

### <a name="nqueries--int"></a>nqueries: [int](xref:microsoft.quantum.lang-ref.int)

Anzahl von Abfragen für das Zustands Vorbereitungs-Oracle. Muss eine ungerade ganze Zahl sein.


### <a name="successmin--double"></a>Erfolg: [Double](xref:microsoft.quantum.lang-ref.double)

Die minimale Erfolgswahrscheinlichkeit für das Ziel.



## <a name="output--reflectionphases"></a>Ausgabe: [reflectionphasen](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)

Ein Array von Phasen, das in der Implementierung eines Quantum-Algorithmus für die fest Komma Verstärkung verwendet werden kann.

## <a name="references"></a>Referenzen

Wir verwenden die Phasen in "Verstärkung mit fester Punkt Amplitude mit einer optimalen Anzahl von Abfragen".

- [YoderLowChuang2014](https://arxiv.org/abs/1409.3305) Siehe auch "Methodik von zusammengesetzten quantgates"
- [LowYoderChuang2016](https://arxiv.org/abs/1603.03996) für Phasen im `RotationPhases` Format.
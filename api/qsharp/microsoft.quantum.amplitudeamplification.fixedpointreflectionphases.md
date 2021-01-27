---
uid: Microsoft.Quantum.AmplitudeAmplification.FixedPointReflectionPhases
title: Fixedpointreflectionphasen-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: FixedPointReflectionPhases
qsharp.summary: Computes partial reflection phases for fixed-point amplitude amplification.
ms.openlocfilehash: 2ded197801111c26d8a33f9c2363b46ca4b6c4b9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845854"
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

## <a name="references"></a>References

Wir verwenden die Phasen in "Verstärkung mit fester Punkt Amplitude mit einer optimalen Anzahl von Abfragen".

- [YoderLowChuang2014](https://arxiv.org/abs/1409.3305) Siehe auch "Methodik von zusammengesetzten quantgates"
- [LowYoderChuang2016](https://arxiv.org/abs/1603.03996) für Phasen im `RotationPhases` Format.
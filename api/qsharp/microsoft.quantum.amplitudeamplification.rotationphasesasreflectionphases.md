---
uid: Microsoft.Quantum.AmplitudeAmplification.RotationPhasesAsReflectionPhases
title: Rotationphasesasreflectionphasen-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: RotationPhasesAsReflectionPhases
qsharp.summary: Converts phases specified as single-qubit rotations to phases specified as partial reflections.
ms.openlocfilehash: 6e601cfd867b449d628da7cd60dfacd465e48860
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191192"
---
# <a name="rotationphasesasreflectionphases-function"></a>Rotationphasesasreflectionphasen-Funktion

Namespace: [Microsoft. Quantum. Verstärkungs Verstärkung](xref:Microsoft.Quantum.AmplitudeAmplification)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Konvertiert als Single-Qubit-Drehungen angegebene Phasen in Phasen, die als partielle Reflektionen angegeben sind.

```qsharp
function RotationPhasesAsReflectionPhases (rotPhases : Microsoft.Quantum.AmplitudeAmplification.RotationPhases) : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
```


## <a name="input"></a>Eingabe

### <a name="rotphases--rotationphases"></a>rotphasen: [rotationphasen](xref:Microsoft.Quantum.AmplitudeAmplification.RotationPhases)

Array von Single-Qubit-Drehungen, das in partielle Reflektionen konvertiert werden soll.



## <a name="output--reflectionphases"></a>Ausgabe: [reflectionphasen](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)

Ein Vorgang, der Phasen implementiert, die als Teil Spiegelungen angegeben werden.

## <a name="references"></a>Referenzen

Wir verwenden die Konvention in

- [ *G.H. Low, I. L. Chuang*](https://arxiv.org/abs/1707.05391) zum Verknüpfen von Single-Qubit-Rotations Phasen mit reflektionsoperator-Phasen.
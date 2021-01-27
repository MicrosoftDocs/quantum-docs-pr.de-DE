---
uid: Microsoft.Quantum.AmplitudeAmplification.RotationPhasesAsReflectionPhases
title: Rotationphasesasreflectionphasen-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: RotationPhasesAsReflectionPhases
qsharp.summary: Converts phases specified as single-qubit rotations to phases specified as partial reflections.
ms.openlocfilehash: 5d50b3fdc2b0f948e93cb11b5c69403d97574ccd
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843957"
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

## <a name="references"></a>References

Wir verwenden die Konvention in

- [ *G.H. Low, I. L. Chuang*](https://arxiv.org/abs/1707.05391) zum Verknüpfen von Single-Qubit-Rotations Phasen mit reflektionsoperator-Phasen.
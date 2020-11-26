---
uid: Microsoft.Quantum.AmplitudeAmplification.RotationPhases
title: Benutzerdefinierter Typ "rotationphasen"
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: RotationPhases
qsharp.summary: Phases for a sequence of single-qubit rotations in amplitude amplification.
ms.openlocfilehash: 60fcda7d58a19f8891e252ddb18b504afddf5514
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191362"
---
# <a name="rotationphases-user-defined-type"></a>Benutzerdefinierter Typ "rotationphasen"

Namespace: [Microsoft. Quantum. Verstärkungs Verstärkung](xref:Microsoft.Quantum.AmplitudeAmplification)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Phasen für eine Sequenz von Single-Qubit-Drehungen in der Amplitude-Verstärkung.

```qsharp

newtype RotationPhases = (Double[]);
```



## <a name="remarks"></a>Bemerkungen

Der erste Parameter ist ein Array von Phasen für Reflektionen, ausgedrückt als Produkt von Single-Qubit-Drehungen.
[G.H. Niedrig, I. L. Chuang, https://arxiv.org/abs/1707.05391 ].
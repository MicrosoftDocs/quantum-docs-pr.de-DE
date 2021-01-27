---
uid: Microsoft.Quantum.AmplitudeAmplification.RotationPhases
title: Benutzerdefinierter Typ "rotationphasen"
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: RotationPhases
qsharp.summary: Phases for a sequence of single-qubit rotations in amplitude amplification.
ms.openlocfilehash: 2f955ce3bfb9ea057c26c79547895df39ed322ab
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843962"
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
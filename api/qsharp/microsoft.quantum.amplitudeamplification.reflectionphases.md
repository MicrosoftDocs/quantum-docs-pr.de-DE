---
uid: Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
title: Reflectionphasen-benutzerdefinierter Typ
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ReflectionPhases
qsharp.summary: Phases for a sequence of partial reflections in amplitude amplification.
ms.openlocfilehash: 743ece778239c223573a3a8536ae8059cea09d5f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191345"
---
# <a name="reflectionphases-user-defined-type"></a>Reflectionphasen-benutzerdefinierter Typ

Namespace: [Microsoft. Quantum. Verstärkungs Verstärkung](xref:Microsoft.Quantum.AmplitudeAmplification)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Phasen für eine Sequenz von partiellen Reflektionen bei der Amplitude-Verstärkung.

```qsharp

newtype ReflectionPhases = (AboutStart : Double[], AboutTarget : Double[]);
```



## <a name="named-items"></a>Benannte Elemente

### <a name="aboutstart--double"></a>Aboutstart: [Double](xref:microsoft.quantum.lang-ref.double)[]

Ein Array von Phasen für die Reflektion über den Startzustand.
### <a name="abouttarget--double"></a>Abouttarget: [Double](xref:microsoft.quantum.lang-ref.double)[]

Ein Array von Phasen für die Reflektion über den Zielzustand.

## <a name="remarks"></a>Bemerkungen

Beide Arrays müssen die gleiche Länge aufweisen. Beachten Sie, dass in vielen Fällen in der ersten Phase für den Startstatus und die letzte Phase zum Ziel Status eine globale Phasenverschiebung eingeführt und möglicherweise auf $0 $ festgelegt wird.
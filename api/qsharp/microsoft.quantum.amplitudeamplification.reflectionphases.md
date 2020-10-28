---
uid: Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
title: Reflectionphasen-benutzerdefinierter Typ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ReflectionPhases
qsharp.summary: Phases for a sequence of partial reflections in amplitude amplification.
ms.openlocfilehash: e0c7db6cd1aad636a34684958be117de1b9888f8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92721814"
---
# <a name="reflectionphases-user-defined-type"></a>Reflectionphasen-benutzerdefinierter Typ

Namespace: [Microsoft. Quantum. Verstärkungs Verstärkung](xref:Microsoft.Quantum.AmplitudeAmplification)

Paketen [](https://nuget.org/packages/)


Phasen für eine Sequenz von partiellen Reflektionen bei der Amplitude-Verstärkung.

```qsharp

newtype ReflectionPhases = (AboutStart : Double[], AboutTarget : Double[]);
```



## <a name="named-items"></a>Benannte Elemente

### <a name="aboutstart--double"></a>Aboutstart: [Double](xref:microsoft.quantum.lang-ref.double)[]

Ein Array von Phasen für die Reflektion über den Startzustand.
### <a name="abouttarget--double"></a>Abouttarget: [Double](xref:microsoft.quantum.lang-ref.double)[]

Ein Array von Phasen für die Reflektion über den Zielzustand.

## <a name="remarks"></a>Hinweise

Beide Arrays müssen die gleiche Länge aufweisen. Beachten Sie, dass in vielen Fällen in der ersten Phase für den Startstatus und die letzte Phase zum Ziel Status eine globale Phasenverschiebung eingeführt und möglicherweise auf $0 $ festgelegt wird.
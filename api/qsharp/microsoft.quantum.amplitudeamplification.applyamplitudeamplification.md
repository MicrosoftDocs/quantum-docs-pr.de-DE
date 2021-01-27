---
uid: Microsoft.Quantum.AmplitudeAmplification.ApplyAmplitudeAmplification
title: Applyverstärktudeverstärkungsvorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ApplyAmplitudeAmplification
qsharp.summary: Applies amplitude amplification on a given register, using a given set of phases and oracles to reflect about the initial and final states.
ms.openlocfilehash: 8fd5c3f20c5a5aaae140feaf3af02395bff77b9c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845881"
---
# <a name="applyamplitudeamplification-operation"></a>Applyverstärktudeverstärkungsvorgang

Namespace: [Microsoft. Quantum. Verstärkungs Verstärkung](xref:Microsoft.Quantum.AmplitudeAmplification)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Wendet die Amplitude-Verstärkung für ein angegebenes Register an, wobei eine bestimmte Reihe von Phasen und Oracles verwendet werden, um den ursprünglichen und den Endzustand widerzuspiegeln.

```qsharp
operation ApplyAmplitudeAmplification (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, startStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, targetStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, target : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Eingabe

### <a name="phases--reflectionphases"></a>Phasen: [reflectionphasen](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)

Ein Satz von Phasen, in denen die partiellen Reflektionen bei jedem Schritt des Amplitude-Verstärkungs Algorithmus beschrieben werden. Ein Beispiel finden Sie unter @"microsoft.quantum.amplitudeamplification.standardreflectionphases".


### <a name="startstatereflection--reflectionoracle"></a>Startstatus-eflection: [reflectionoracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)

Ein Oracle, das den ursprünglichen Zustand reflektiert.


### <a name="targetstatereflection--reflectionoracle"></a>targetstatuereflection: [reflectionoracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)

Ein Oracle, das den gewünschten Endzustand reflektiert.


### <a name="target--qubit"></a>Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Ein Register zum Durchführen der Amplitude-Verstärkung.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)


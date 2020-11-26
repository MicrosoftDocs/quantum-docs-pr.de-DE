---
uid: Microsoft.Quantum.AmplitudeAmplification.ObliviousAmplitudeAmplificationFromPartialReflections
title: Obliviousamplitubinverstärkationfrompartialreflections-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ObliviousAmplitudeAmplificationFromPartialReflections
qsharp.summary: Returns a unitary that implements oblivious amplitude amplification by specifying for partial reflections.
ms.openlocfilehash: c818fcd8d8b83d8b479b4f133497449d500ca70e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191311"
---
# <a name="obliviousamplitudeamplificationfrompartialreflections-function"></a>Obliviousamplitubinverstärkationfrompartialreflections-Funktion

Namespace: [Microsoft. Quantum. Verstärkungs Verstärkung](xref:Microsoft.Quantum.AmplitudeAmplification)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt eine einheitliche zurück, die die Verstärkung der Amplitude durch die Angabe von für partielle Reflektionen implementiert.

```qsharp
function ObliviousAmplitudeAmplificationFromPartialReflections (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, startStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, targetStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, signalOracle : Microsoft.Quantum.Oracles.ObliviousOracle) : ((Qubit[], Qubit[]) => Unit is Adj + Ctl)
```


## <a name="input"></a>Eingabe

### <a name="phases--reflectionphases"></a>Phasen: [reflectionphasen](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)




### <a name="startstatereflection--reflectionoracle"></a>Startstatus-eflection: [reflectionoracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)




### <a name="targetstatereflection--reflectionoracle"></a>targetstatuereflection: [reflectionoracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)




### <a name="signaloracle--obliviousoracle"></a>signaloracle: [obliviousoracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)





## <a name="output--qubitqubit--unit--is-adj--ctl"></a>Ausgabe: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL


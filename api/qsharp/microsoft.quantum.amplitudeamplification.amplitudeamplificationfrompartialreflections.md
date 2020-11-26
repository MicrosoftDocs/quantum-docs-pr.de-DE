---
uid: Microsoft.Quantum.AmplitudeAmplification.AmplitudeAmplificationFromPartialReflections
title: Amplitubinverstärkficationfrompartialreflections-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: AmplitudeAmplificationFromPartialReflections
qsharp.summary: Amplitude amplification by partial reflections.
ms.openlocfilehash: 8fa6db7d5616f8c561191e3da00a69b05041b279
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191685"
---
# <a name="amplitudeamplificationfrompartialreflections-function"></a>Amplitubinverstärkficationfrompartialreflections-Funktion

Namespace: [Microsoft. Quantum. Verstärkungs Verstärkung](xref:Microsoft.Quantum.AmplitudeAmplification)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Amplitude-Verstärkung durch partielle Reflektionen.

```qsharp
function AmplitudeAmplificationFromPartialReflections (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, startStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, targetStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a>Eingabe

### <a name="phases--reflectionphases"></a>Phasen: [reflectionphasen](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)

Phasen von partiellen Reflektionen


### <a name="startstatereflection--reflectionoracle"></a>Startstatus-eflection: [reflectionoracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)

Reflektionsoperator zum Startstatus


### <a name="targetstatereflection--reflectionoracle"></a>targetstatuereflection: [reflectionoracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)

Reflektionsoperator zum Ziel Status



## <a name="output--qubit--unit--is-adj--ctl"></a>Ausgabe: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL

Ein Vorgang, der die Amplitude-Verstärkung durch partielle Reflektionen implementiert.

## <a name="remarks"></a>Bemerkungen

Die Amplitude-Verstärkung ist ein Sonderfall der Zerlegung von Amplitude, bei der keine System-Qubits vorhanden sind und das schrägende Oracle auf Identity festgelegt ist.
In den meisten Fällen `startQubits` wird im Status $ \ket{\text{Start}} $1 initialisiert \_ . Dies ist der $-$1-eigen Zustand von `startStateReflection` .
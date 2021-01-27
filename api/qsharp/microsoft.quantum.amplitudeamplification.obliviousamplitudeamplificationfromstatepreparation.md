---
uid: Microsoft.Quantum.AmplitudeAmplification.ObliviousAmplitudeAmplificationFromStatePreparation
title: Obliviousamplitubinverstärkationfromstatepreparation-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ObliviousAmplitudeAmplificationFromStatePreparation
qsharp.summary: Oblivious amplitude amplification by oracles for partial reflections.
ms.openlocfilehash: 873c436d4b8d8efc9dc61c2baba9b0e0f7f09fc2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845823"
---
# <a name="obliviousamplitudeamplificationfromstatepreparation-function"></a>Obliviousamplitubinverstärkationfromstatepreparation-Funktion

Namespace: [Microsoft. Quantum. Verstärkungs Verstärkung](xref:Microsoft.Quantum.AmplitudeAmplification)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Pervirone Amplitude-Verstärkung durch Oracles für partielle Reflektionen.

```qsharp
function ObliviousAmplitudeAmplificationFromStatePreparation (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, startStateOracle : Microsoft.Quantum.Oracles.DeterministicStateOracle, signalOracle : Microsoft.Quantum.Oracles.ObliviousOracle, idxFlagQubit : Int) : ((Qubit[], Qubit[]) => Unit is Adj + Ctl)
```


## <a name="input"></a>Eingabe

### <a name="phases--reflectionphases"></a>Phasen: [reflectionphasen](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)

Phasen von partiellen Reflektionen


### <a name="startstateoracle--deterministicstateoracle"></a>startstateoracle: [deterministicstateoracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)

Einheitlicher Oracle-$A $, der den Status des zusätzlichen Starts vorbereitet


### <a name="signaloracle--obliviousoracle"></a>signaloracle: [obliviousoracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)

Einheitlicher Oracle-$O $ vom Typ `ObliviousOracle` , der gemeinsam mit dem Hilfssystem und dem System Register agiert


### <a name="idxflagqubit--int"></a>idxflagqubit: [int](xref:microsoft.quantum.lang-ref.int)

Index für Single-Qubit-Flag-Register



## <a name="output--qubitqubit--unit--is-adj--ctl"></a>Ausgabe: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL

Ein Vorgang, der die pervirone Amplitude-Verstärkung basierend auf partiellen Reflektionen implementiert.

## <a name="remarks"></a>Bemerkungen

Dies erzwingt strengere Bedingungen in Form der zusätzlichen Start-und Ziel Zustände als in `AmpAmpObliviousByReflectionPhases` .
Es wird davon ausgegangen, dass $A \ket {0} \_ f \ket {0} \_ A = \ket{\text{Start}} \_ {FA} $ den zusätzlichen Startstatus $ \ket{\text{Start}} \_ {FA} $ von der Berechnungsbasis $ \ket {0} \_ f \ket {0} $ vorbereitet.
Es wird davon ausgegangen, dass der Ziel Status durch "$ \ket f $" gekennzeichnet ist {1} \_ .
Es wird davon ausgegangen, dass \begin{align} o\ket {\ Text {Start}} \_ {FA} \ket{\psi} \_ s = \lambda\ket {1} \_ f \ket {\ Text {Anything}} \_ a\ket {\ Text {Target}} \_ s U \ket{\psi} \_ s + \sqrt{1-| \lambda | ^ 2} \ket {0} \_ f \ cdots, \end{align} für einige einheitliche $U $.
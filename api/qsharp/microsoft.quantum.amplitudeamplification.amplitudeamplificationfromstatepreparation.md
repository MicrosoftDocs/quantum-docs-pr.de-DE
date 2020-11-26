---
uid: Microsoft.Quantum.AmplitudeAmplification.AmplitudeAmplificationFromStatePreparation
title: Verstärkungsfromstatepreparation-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: AmplitudeAmplificationFromStatePreparation
qsharp.summary: Amplitude amplification by oracles for partial reflections.
ms.openlocfilehash: 30e1cf6e353b8a4491e13a9e2f588ec9cc103cb4
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191600"
---
# <a name="amplitudeamplificationfromstatepreparation-function"></a>Verstärkungsfromstatepreparation-Funktion

Namespace: [Microsoft. Quantum. Verstärkungs Verstärkung](xref:Microsoft.Quantum.AmplitudeAmplification)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Amplitude-Verstärkung durch Oracles für partielle Reflektionen.

```qsharp
function AmplitudeAmplificationFromStatePreparation (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, stateOracle : Microsoft.Quantum.Oracles.StateOracle, idxFlagQubit : Int) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a>Eingabe

### <a name="phases--reflectionphases"></a>Phasen: [reflectionphasen](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)

Phasen von partiellen Reflektionen


### <a name="stateoracle--stateoracle"></a>stateoracle: [stateoracle](xref:Microsoft.Quantum.Oracles.StateOracle)

Einheitlicher Oracle-$A $, der den Startstatus vorbereitet


### <a name="idxflagqubit--int"></a>idxflagqubit: [int](xref:microsoft.quantum.lang-ref.int)

Index zum Markieren von Qubit



## <a name="output--qubit--unit--is-adj--ctl"></a>Ausgabe: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL

Ein Vorgang, der die Amplitude-Verstärkung durch Oracles implementiert, die von partiellen Reflektionen implementiert werden.

## <a name="remarks"></a>Bemerkungen

Dies erzwingt strengere Bedingungen in Form von Start-und Ziel Zuständen als in `AmpAmpByReflectionPhases` .
Es wird davon ausgegangen, dass der Ziel Status durch "$ \ket f $" gekennzeichnet ist {1} \_ .
Es wird davon ausgegangen, dass "\begin{align} a\ket {0} \_ {f} \ket {0} \_ s = \lambda\ket {1} \_ f \ket {\ Text {Target}} \_ s + \sqrt{1-| \lambda | ^ 2} \ket {0} \_ f \ cdots" lautet, \end{align} in den meisten Fällen `flagQubit` und `auxiliaryRegister` werden im Status $ \ket {0} \_ {f} \ket {0} \_ s $ initialisiert.
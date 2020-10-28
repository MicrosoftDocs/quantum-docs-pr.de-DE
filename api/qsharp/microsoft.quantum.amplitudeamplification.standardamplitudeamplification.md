---
uid: Microsoft.Quantum.AmplitudeAmplification.StandardAmplitudeAmplification
title: Standardamplituentverstärkungsfunktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: StandardAmplitudeAmplification
qsharp.summary: Standard Amplitude Amplification algorithm
ms.openlocfilehash: 18228d45c4df280b004c595a7b0f1e2a607b8b2c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92721744"
---
# <a name="standardamplitudeamplification-function"></a>Standardamplituentverstärkungsfunktion

Namespace: [Microsoft. Quantum. Verstärkungs Verstärkung](xref:Microsoft.Quantum.AmplitudeAmplification)

Paketen [](https://nuget.org/packages/)


Standard mäßiger Amplitude-Verstärkungs Algorithmus

```qsharp
function StandardAmplitudeAmplification (nIterations : Int, stateOracle : Microsoft.Quantum.Oracles.StateOracle, idxFlagQubit : Int) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a>Eingabe

### <a name="niterations--int"></a>niterationen: [int](xref:microsoft.quantum.lang-ref.int)

Anzahl der Iterationen $n $ der Amplitude-Verstärkung


### <a name="stateoracle--stateoracle"></a>stateoracle: [stateoracle](xref:Microsoft.Quantum.Oracles.StateOracle)

Einheitlicher Oracle-$A $, der den Startstatus vorbereitet


### <a name="idxflagqubit--int"></a>idxflagqubit: [int](xref:microsoft.quantum.lang-ref.int)

Index zum Markieren von Qubit



## <a name="output--qubit--unit-adj--ctl"></a>Ausgabe: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL

Ein Vorgang, der den standardmäßigen Amplitude-Verstärkungs Algorithmus implementiert.

## <a name="remarks"></a>Hinweise

Dies ist der standardmäßige Amplitude-Verstärkungs Algorithmus, der durch eine Auswahl von Reflexionsphasen erzielt wird, die durch `AmpAmpPhasesStandard` die Annahme berechnet werden, dass "\begin{align} a\ket {0} \_ {f} \ket {0} \_ s = \lambda\ket {1} \_ f \ket {\ Text {Target}} \_ s + \sqrt{1-| \lambda | ^ 2} \ket- {0} \_ \end{align} dieser Vorgang bereitet den Status" \begin{align} \operatorname{AmpAmpByOracle}\ket {0} \_ {f} \ket {0} \_ s = \sin ((2n + 1) \sin ^ {-1} (\lambda)) \ket {1} \_ f \ket {\ Text {Target}} \_ s + \cdoz\ket {0} \_ f \end{align} "in den meisten Fällen vor. `flagQubit` und werden `auxiliaryRegister` im Zustand" $ \ket {0} \_ f \ket {0} \_ a $ "initialisiert.

## <a name="references"></a>Referenzen

- [*G. Brassard, P. Hoyer, M. Musca, A. Tapp*](https://arxiv.org/abs/quant-ph/0005055)
---
uid: Microsoft.Quantum.AmplitudeAmplification.ApplyObliviousAmplitudeAmplification
title: Applyobliviousamplitudeverstärkungsvorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ApplyObliviousAmplitudeAmplification
qsharp.summary: Oblivious amplitude amplification by specifying partial reflections.
ms.openlocfilehash: a1bda344b1097c7ab3240bc6d9cd0d8df80b9662
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92721883"
---
# <a name="applyobliviousamplitudeamplification-operation"></a>Applyobliviousamplitudeverstärkungsvorgang

Namespace: [Microsoft. Quantum. Verstärkungs Verstärkung](xref:Microsoft.Quantum.AmplitudeAmplification)

Paketen [](https://nuget.org/packages/)


Durch die Angabe partieller Reflektionen wird die Verstärkung der Amplitude-Verstärkung unterstreicht

```qsharp
operation ApplyObliviousAmplitudeAmplification (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, startStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, targetStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, signalOracle : Microsoft.Quantum.Oracles.ObliviousOracle, auxiliaryRegister : Qubit[], systemRegister : Qubit[]) : Unit
```


## <a name="input"></a>Eingabe

### <a name="phases--reflectionphases"></a>Phasen: [reflectionphasen](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)

Phasen von partiellen Reflektionen


### <a name="startstatereflection--reflectionoracle"></a>Startstatus-eflection: [reflectionoracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)

Reflektionsoperator zum Startstatus des Zusatz Registers


### <a name="targetstatereflection--reflectionoracle"></a>targetstatuereflection: [reflectionoracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)

Reflektionsoperator zum Ziel Status des Zusatz Registers


### <a name="signaloracle--obliviousoracle"></a>signaloracle: [obliviousoracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)

Einheitlicher Oracle-$O $ vom Typ `ObliviousOracle` , der gemeinsam auf dem Hilfssystem und dem System Register agiert.


### <a name="auxiliaryregister--qubit"></a>auxiliaryregister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Zusatz Register


### <a name="systemregister--qubit"></a>Systemregister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

System Register



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Hinweise

Bei einem bestimmten Zusatz Status $ \ket{\text{Start}} \_ a $, einem bestimmten Zusatz Ziel Status $ \ket{\text{Target}} \_ a $ und jedem Systemstatus $ \ket{\psi} \_ s $, angenommen, \begin{align} o\ket {\ Text {Start}} \_ a\ket {\ PSI} \_ s = \lambda\ket{\text{Target}} \_ a U \ket{\psi} \_ s + \sqrt{1-| \lambda | ^ 2} \ket{\text{Target} ^ \perp} \_ a\cdots \end{align} für einige einheitliche $U $.
Durch eine Sequenz von Reflektionen zu den Start-und Ziel Zuständen im Zusatz Register, die von Anwendungen von `signalOracle` und dessen Adjoint überschneidet werden, kann die Erfolgswahrscheinlichkeit der Anwendung U geändert werden.

In den meisten Fällen `auxiliaryRegister` wird im Status $ \ket{\text{Start}} \_ a $ initialisiert.

## <a name="references"></a>Referenzen

Siehe

- [ *D.W. Berry, Uhr Childs, r. Cleve, r. Kothari, R.D. Somma*](https://arxiv.org/abs/1312.1414) für die Standardversion.
  Siehe
- [ *G.H. Low, I.L. Chuang*](https://arxiv.org/abs/1610.06546) for a Generalisierung to partielle Reflektionen.
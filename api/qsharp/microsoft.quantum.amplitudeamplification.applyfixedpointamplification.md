---
uid: Microsoft.Quantum.AmplitudeAmplification.ApplyFixedPointAmplification
title: Applyfixedpoinmanipulieren-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ApplyFixedPointAmplification
qsharp.summary: Fixed-Point Amplitude Amplification algorithm
ms.openlocfilehash: f506be7b2e3f65cf89694e30d79c04ec30d25035
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92721911"
---
# <a name="applyfixedpointamplification-operation"></a>Applyfixedpoinmanipulieren-Vorgang

Namespace: [Microsoft. Quantum. Verstärkungs Verstärkung](xref:Microsoft.Quantum.AmplitudeAmplification)

Paketen [](https://nuget.org/packages/)


Fixed-Point Amplitude-Verstärkungs Algorithmus

```qsharp
operation ApplyFixedPointAmplification (statePrepOracle : Microsoft.Quantum.Oracles.StateOracle, startQubits : Qubit[]) : Unit
```


## <a name="input"></a>Eingabe

### <a name="statepreporacle--stateoracle"></a>statepreporacle: [stateoracle](xref:Microsoft.Quantum.Oracles.StateOracle)

Einheitliches Oracle, das den Startstatus vorbereitet.


### <a name="startqubits--qubit"></a>startqubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Qubit-Register



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Hinweise

Startqubits muss sich im Status $ \ket{0\cdots 0} $ befinden. Dieser Vorgang durchläuft eine Reihe von Abfragen in den Befugnissen von $2 $, bis entweder eine maximale Anzahl von Abfragen erreicht oder der Ziel Status gefunden wird.
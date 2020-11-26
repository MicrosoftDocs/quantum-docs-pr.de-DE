---
uid: Microsoft.Quantum.AmplitudeAmplification.ApplyFixedPointAmplification
title: Applyfixedpoinmanipulieren-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ApplyFixedPointAmplification
qsharp.summary: Fixed-Point Amplitude Amplification algorithm
ms.openlocfilehash: 13e70b1ebd5e3bf0996e6a76f4bffe57ca2d2250
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191532"
---
# <a name="applyfixedpointamplification-operation"></a>Applyfixedpoinmanipulieren-Vorgang

Namespace: [Microsoft. Quantum. Verstärkungs Verstärkung](xref:Microsoft.Quantum.AmplitudeAmplification)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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



## <a name="remarks"></a>Bemerkungen

Startqubits muss sich im Status $ \ket{0\cdots 0} $ befinden. Dieser Vorgang durchläuft eine Reihe von Abfragen in den Befugnissen von $2 $, bis entweder eine maximale Anzahl von Abfragen erreicht oder der Ziel Status gefunden wird.
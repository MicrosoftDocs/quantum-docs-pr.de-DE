---
uid: Microsoft.Quantum.Simulation.TrotterStep
title: Trotterstep-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TrotterStep
qsharp.summary: Implements a single time-step of time-evolution by the system described in an `EvolutionGenerator` using a Trotter–Suzuki decomposition.
ms.openlocfilehash: 7a1a27ba4dc4b8b7bbc4da6a378d4a1494bc9415
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725355"
---
# <a name="trotterstep-function"></a>Trotterstep-Funktion

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paketen [](https://nuget.org/packages/)


Implementiert einen einzelnen Zeit Schritt der Zeitentwicklung durch das in einer `EvolutionGenerator` mithilfe einer Trotter – Suzuki-Zerlegung beschriebene System.

```qsharp
function TrotterStep (evolutionGenerator : Microsoft.Quantum.Simulation.EvolutionGenerator, trotterOrder : Int, trotterStepSize : Double) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a>Eingabe

### <a name="evolutiongenerator--evolutiongenerator"></a>evolutiongenerator: [evolutiongenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)

Eine umfassende Beschreibung des Systems, das simuliert werden soll.


### <a name="trotterorder--int"></a>trotterorder: [int](xref:microsoft.quantum.lang-ref.int)

Reihenfolge des trockintegrator. Dies muss entweder 1 oder eine gerade Zahl sein.


### <a name="trotterstepsize--double"></a>trotterstepsize: [Double](xref:microsoft.quantum.lang-ref.double)

Dauer der simulierten Zeitentwicklung in einem einzelnen trockschritt.



## <a name="output--qubit--unit-adj--ctl"></a>Ausgabe: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL

Einheitlicher Vorgang, der einen einzelnen Schritt der Zeit-Evolution für die Dauer angleicht `trotterStepSize` .

## <a name="remarks"></a>Hinweise

Weitere Informationen zur Trotter – Suzuki-Zerlegung finden Sie unter [Zeit geordnete Komposition](/quantum/libraries/control-flow#time-ordered-composition).
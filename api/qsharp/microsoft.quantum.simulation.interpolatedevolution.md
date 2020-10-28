---
uid: Microsoft.Quantum.Simulation.InterpolatedEvolution
title: Interpolatedevolution-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: InterpolatedEvolution
qsharp.summary: Interpolates between two generators with a uniform schedule, returning an operation that applies simulated evolution under the resulting time-dependent generator to a qubit register.
ms.openlocfilehash: 18026b9872f6a3344a1e5c2122f55927975ccb59
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701730"
---
# <a name="interpolatedevolution-function"></a>Interpolatedevolution-Funktion

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paketen [](https://nuget.org/packages/)


Interpoliert zwischen zwei Generatoren mit einem einheitlichen Zeitplan und gibt einen Vorgang zurück, der die simulierte Weiterentwicklung unter dem resultierenden zeitabhängigen Generator auf ein Qubit-Register anwendet.

```qsharp
function InterpolatedEvolution (interpolationTime : Double, evolutionGeneratorStart : Microsoft.Quantum.Simulation.EvolutionGenerator, evolutionGeneratorEnd : Microsoft.Quantum.Simulation.EvolutionGenerator, timeDependentSimulationAlgorithm : Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a>Eingabe

### <a name="interpolationtime--double"></a>interpolationtime: [Double](xref:microsoft.quantum.lang-ref.double)

Zeit zum Ausführen der Interpolations Zeit.


### <a name="evolutiongeneratorstart--evolutiongenerator"></a>evolutiongeneratorstart: [evolutiongenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)

Ursprünglicher Generator, unter dem die Entwicklung simuliert werden soll.


### <a name="evolutiongeneratorend--evolutiongenerator"></a>evolutiongeneratorend: [evolutiongenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)

Der endgültige Generator, unter dem die Entwicklung simuliert werden soll.


### <a name="timedependentsimulationalgorithm--timedependentsimulationalgorithm"></a>timedependentsimulationalgorithmus: [timedependentsimulationalgorithmus](xref:Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm)

Ein zeitabhängiger Simulations Algorithmus, der verwendet wird, um die Evolution während des einheitlichen Interpolations Zeitplans zu simulieren.



## <a name="output--qubit--unit-adj--ctl"></a>Ausgabe: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL



## <a name="remarks"></a>Hinweise

Wenn die Interpolations Zeit ausgewählt ist, um die adiabatischen Bedingungen zu erfüllen, gibt diese Funktion einen Vorgang zurück, der die adiabatische Zustands Vorbereitung für den endgültigen Dynamical-Generator ausführt.
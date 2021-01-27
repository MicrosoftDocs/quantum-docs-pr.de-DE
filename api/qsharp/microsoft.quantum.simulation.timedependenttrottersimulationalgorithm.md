---
uid: Microsoft.Quantum.Simulation.TimeDependentTrotterSimulationAlgorithm
title: Timedependenttrottersimulationalgorithmus-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TimeDependentTrotterSimulationAlgorithm
qsharp.summary: '`TimeDependentSimulationAlgorithm` function that uses a Trotter–Suzuki decomposition to approximate a unitary operator that solves the time-dependent Schrodinger equation.'
ms.openlocfilehash: c827dd79af6f4b745adf8903ed2664d9e8255785
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858358"
---
# <a name="timedependenttrottersimulationalgorithm-function"></a>Timedependenttrottersimulationalgorithmus-Funktion

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


`TimeDependentSimulationAlgorithm` eine Funktion, die eine Trotter – Suzuki-Zerlegung verwendet, um einen einheitlichen Operator zu nähern, der die zeitabhängige Schrodinger-Gleichung löst.

```qsharp
function TimeDependentTrotterSimulationAlgorithm (trotterStepSize : Double, trotterOrder : Int) : Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm
```


## <a name="input"></a>Eingabe

### <a name="trotterstepsize--double"></a>trotterstepsize: [Double](xref:microsoft.quantum.lang-ref.double)

Dauer der simulierten Zeitentwicklung in einem einzelnen trockschritt.


### <a name="trotterorder--int"></a>trotterorder: [int](xref:microsoft.quantum.lang-ref.int)

Reihenfolge des trockintegrator. Dies muss entweder 1 oder eine gerade Zahl sein.



## <a name="output--timedependentsimulationalgorithm"></a>Ausgabe: [timedependentsimulationalgorithmus](xref:Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm)

Ein `TimeDependentSimulationAlgorithm`-Typ.
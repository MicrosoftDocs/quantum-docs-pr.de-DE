---
uid: Microsoft.Quantum.Simulation.TrotterSimulationAlgorithm
title: Trottersimulationalgorithmus-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TrotterSimulationAlgorithm
qsharp.summary: '`SimulationAlgorithm` function that uses a Trotter–Suzuki decomposition to approximate the time-evolution operator _exp(-iHt)_.'
ms.openlocfilehash: aa8338ab359441765db72a12f84a3a51e5bee3ce
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192535"
---
# <a name="trottersimulationalgorithm-function"></a>Trottersimulationalgorithmus-Funktion

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


`SimulationAlgorithm` eine Funktion, die eine Trotter – Suzuki-Zerlegung verwendet, um den Time-Evolution Operator _Exp (-IHT)_ zu annähern.

```qsharp
function TrotterSimulationAlgorithm (trotterStepSize : Double, trotterOrder : Int) : Microsoft.Quantum.Simulation.SimulationAlgorithm
```


## <a name="input"></a>Eingabe

### <a name="trotterstepsize--double"></a>trotterstepsize: [Double](xref:microsoft.quantum.lang-ref.double)

Dauer der simulierten Zeitentwicklung in einem einzelnen trockschritt.


### <a name="trotterorder--int"></a>trotterorder: [int](xref:microsoft.quantum.lang-ref.int)

Reihenfolge des trockintegrator. Dies muss entweder 1 oder eine gerade Zahl sein.



## <a name="output--simulationalgorithm"></a>Ausgabe: [simulationalgorithmus](xref:Microsoft.Quantum.Simulation.SimulationAlgorithm)

Ein `SimulationAlgorithm`-Typ.
---
uid: Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm
title: Benutzerdefinierter timedependentsimulationalgorithmus-Typ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TimeDependentSimulationAlgorithm
qsharp.summary: >-
  Represents a time-dependent simulation algorithm.

  A time-dependent simulation technique converts an <xref:microsoft.quantum.simulation.evolutionschedule> to unitary time-evolution for some time-interval.
ms.openlocfilehash: 9d2a1a853005495b5a9df60ac1f0dcbfbdf7637f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725748"
---
# <a name="timedependentsimulationalgorithm-user-defined-type"></a>Benutzerdefinierter timedependentsimulationalgorithmus-Typ

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paketen [](https://nuget.org/packages/)


Stellt einen zeitabhängigen Simulations Algorithmus dar.

Eine zeitabhängige Simulationstechnik konvertiert ein <xref:microsoft.quantum.simulation.evolutionschedule>
zur einheitlichen Zeit-Evolution für einige Zeitintervalle.

```qsharp

newtype TimeDependentSimulationAlgorithm = (((Double, Microsoft.Quantum.Simulation.EvolutionSchedule, Qubit[]) => Unit is Adj + Ctl));
```


---
uid: Microsoft.Quantum.Simulation.SimulationAlgorithm
title: Benutzerdefinierter simulationalgorithmustyp
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: SimulationAlgorithm
qsharp.summary: >-
  Represents a time-independent simulation algorithm.

  A time-independent simulation technique converts an <xref:microsoft.quantum.simulation.evolutiongenerator> to unitary time evolution for some time-interval.
ms.openlocfilehash: 9127a936bbf7a212e712645eabdf49fefc7a97d0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725566"
---
# <a name="simulationalgorithm-user-defined-type"></a>Benutzerdefinierter simulationalgorithmustyp

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paketen [](https://nuget.org/packages/)


Stellt einen zeitunabhängigen Simulations Algorithmus dar.

Eine zeitunabhängige Simulationstechnik konvertiert ein <xref:microsoft.quantum.simulation.evolutiongenerator>
zur einheitlichen Zeitentwicklung für einige Zeitintervalle.

```qsharp

newtype SimulationAlgorithm = (((Double, Microsoft.Quantum.Simulation.EvolutionGenerator, Qubit[]) => Unit is Adj + Ctl));
```


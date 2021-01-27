---
uid: Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm
title: Benutzerdefinierter timedependentsimulationalgorithmus-Typ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TimeDependentSimulationAlgorithm
qsharp.summary: >-
  Represents a time-dependent simulation algorithm.

  A time-dependent simulation technique converts an <xref:microsoft.quantum.simulation.evolutionschedule> to unitary time-evolution for some time-interval.
ms.openlocfilehash: 4f393c958e686f2ded3bf3372ff9fd52b2a363cd
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854138"
---
# <a name="timedependentsimulationalgorithm-user-defined-type"></a><span data-ttu-id="10531-102">Benutzerdefinierter timedependentsimulationalgorithmus-Typ</span><span class="sxs-lookup"><span data-stu-id="10531-102">TimeDependentSimulationAlgorithm user defined type</span></span>

<span data-ttu-id="10531-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="10531-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="10531-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="10531-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="10531-105">Stellt einen zeitabhängigen Simulations Algorithmus dar.</span><span class="sxs-lookup"><span data-stu-id="10531-105">Represents a time-dependent simulation algorithm.</span></span>

<span data-ttu-id="10531-106">Eine zeitabhängige Simulationstechnik konvertiert ein <xref:microsoft.quantum.simulation.evolutionschedule></span><span class="sxs-lookup"><span data-stu-id="10531-106">A time-dependent simulation technique converts an <xref:microsoft.quantum.simulation.evolutionschedule></span></span>
<span data-ttu-id="10531-107">zur einheitlichen Zeit-Evolution für einige Zeitintervalle.</span><span class="sxs-lookup"><span data-stu-id="10531-107">to unitary time-evolution for some time-interval.</span></span>

```qsharp

newtype TimeDependentSimulationAlgorithm = (((Double, Microsoft.Quantum.Simulation.EvolutionSchedule, Qubit[]) => Unit is Adj + Ctl));
```


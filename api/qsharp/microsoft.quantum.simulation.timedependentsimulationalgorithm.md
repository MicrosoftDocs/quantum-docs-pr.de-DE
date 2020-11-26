---
uid: Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm
title: Benutzerdefinierter timedependentsimulationalgorithmus-Typ
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TimeDependentSimulationAlgorithm
qsharp.summary: >-
  Represents a time-dependent simulation algorithm.

  A time-dependent simulation technique converts an <xref:microsoft.quantum.simulation.evolutionschedule> to unitary time-evolution for some time-interval.
ms.openlocfilehash: b495a9fd96c78872f84e8f8183105f6290f70655
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192518"
---
# <a name="timedependentsimulationalgorithm-user-defined-type"></a><span data-ttu-id="7198f-102">Benutzerdefinierter timedependentsimulationalgorithmus-Typ</span><span class="sxs-lookup"><span data-stu-id="7198f-102">TimeDependentSimulationAlgorithm user defined type</span></span>

<span data-ttu-id="7198f-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="7198f-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="7198f-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7198f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7198f-105">Stellt einen zeitabhängigen Simulations Algorithmus dar.</span><span class="sxs-lookup"><span data-stu-id="7198f-105">Represents a time-dependent simulation algorithm.</span></span>

<span data-ttu-id="7198f-106">Eine zeitabhängige Simulationstechnik konvertiert ein <xref:microsoft.quantum.simulation.evolutionschedule></span><span class="sxs-lookup"><span data-stu-id="7198f-106">A time-dependent simulation technique converts an <xref:microsoft.quantum.simulation.evolutionschedule></span></span>
<span data-ttu-id="7198f-107">zur einheitlichen Zeit-Evolution für einige Zeitintervalle.</span><span class="sxs-lookup"><span data-stu-id="7198f-107">to unitary time-evolution for some time-interval.</span></span>

```qsharp

newtype TimeDependentSimulationAlgorithm = (((Double, Microsoft.Quantum.Simulation.EvolutionSchedule, Qubit[]) => Unit is Adj + Ctl));
```


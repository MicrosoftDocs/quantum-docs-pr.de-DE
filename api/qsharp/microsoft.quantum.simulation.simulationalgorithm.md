---
uid: Microsoft.Quantum.Simulation.SimulationAlgorithm
title: Benutzerdefinierter simulationalgorithmustyp
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: SimulationAlgorithm
qsharp.summary: >-
  Represents a time-independent simulation algorithm.

  A time-independent simulation technique converts an <xref:microsoft.quantum.simulation.evolutiongenerator> to unitary time evolution for some time-interval.
ms.openlocfilehash: 2f340492b51c97e353cc071d6d563a30a1db86d1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192433"
---
# <a name="simulationalgorithm-user-defined-type"></a><span data-ttu-id="a8de3-102">Benutzerdefinierter simulationalgorithmustyp</span><span class="sxs-lookup"><span data-stu-id="a8de3-102">SimulationAlgorithm user defined type</span></span>

<span data-ttu-id="a8de3-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="a8de3-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="a8de3-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a8de3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a8de3-105">Stellt einen zeitunabhängigen Simulations Algorithmus dar.</span><span class="sxs-lookup"><span data-stu-id="a8de3-105">Represents a time-independent simulation algorithm.</span></span>

<span data-ttu-id="a8de3-106">Eine zeitunabhängige Simulationstechnik konvertiert ein <xref:microsoft.quantum.simulation.evolutiongenerator></span><span class="sxs-lookup"><span data-stu-id="a8de3-106">A time-independent simulation technique converts an <xref:microsoft.quantum.simulation.evolutiongenerator></span></span>
<span data-ttu-id="a8de3-107">zur einheitlichen Zeitentwicklung für einige Zeitintervalle.</span><span class="sxs-lookup"><span data-stu-id="a8de3-107">to unitary time evolution for some time-interval.</span></span>

```qsharp

newtype SimulationAlgorithm = (((Double, Microsoft.Quantum.Simulation.EvolutionGenerator, Qubit[]) => Unit is Adj + Ctl));
```


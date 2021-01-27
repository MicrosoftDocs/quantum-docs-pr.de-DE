---
uid: Microsoft.Quantum.Simulation.SimulationAlgorithm
title: Benutzerdefinierter simulationalgorithmustyp
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: SimulationAlgorithm
qsharp.summary: >-
  Represents a time-independent simulation algorithm.

  A time-independent simulation technique converts an <xref:microsoft.quantum.simulation.evolutiongenerator> to unitary time evolution for some time-interval.
ms.openlocfilehash: d7b233ee76d79072f59ecfd001245848cb780eec
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851042"
---
# <a name="simulationalgorithm-user-defined-type"></a><span data-ttu-id="cd188-102">Benutzerdefinierter simulationalgorithmustyp</span><span class="sxs-lookup"><span data-stu-id="cd188-102">SimulationAlgorithm user defined type</span></span>

<span data-ttu-id="cd188-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="cd188-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="cd188-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cd188-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cd188-105">Stellt einen zeitunabhängigen Simulations Algorithmus dar.</span><span class="sxs-lookup"><span data-stu-id="cd188-105">Represents a time-independent simulation algorithm.</span></span>

<span data-ttu-id="cd188-106">Eine zeitunabhängige Simulationstechnik konvertiert ein <xref:microsoft.quantum.simulation.evolutiongenerator></span><span class="sxs-lookup"><span data-stu-id="cd188-106">A time-independent simulation technique converts an <xref:microsoft.quantum.simulation.evolutiongenerator></span></span>
<span data-ttu-id="cd188-107">zur einheitlichen Zeitentwicklung für einige Zeitintervalle.</span><span class="sxs-lookup"><span data-stu-id="cd188-107">to unitary time evolution for some time-interval.</span></span>

```qsharp

newtype SimulationAlgorithm = (((Double, Microsoft.Quantum.Simulation.EvolutionGenerator, Qubit[]) => Unit is Adj + Ctl));
```


---
uid: Microsoft.Quantum.Simulation.EvolutionSet
title: Benutzerdefinierter evolutionset-Typ
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EvolutionSet
qsharp.summary: >-
  Represents a set of gates that can be readily implemented and used to implement simulation algorithms.

  Elements in the set are indexed by a  <xref:microsoft.quantum.simulation.generatorindex>, and each set is described by a function from `GeneratorIndex` to  <xref:microsoft.quantum.simulation.evolutionunitary>, which are operations parameterized by a real number representing time
ms.openlocfilehash: ee8f3c0716f035dcb0c4fad557092fbf8dd3c356
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229408"
---
# <a name="evolutionset-user-defined-type"></a><span data-ttu-id="4738a-102">Benutzerdefinierter evolutionset-Typ</span><span class="sxs-lookup"><span data-stu-id="4738a-102">EvolutionSet user defined type</span></span>

<span data-ttu-id="4738a-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="4738a-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="4738a-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4738a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4738a-105">Stellt einen Satz von Gates dar, der leicht implementiert und zum Implementieren von Simulations Algorithmen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="4738a-105">Represents a set of gates that can be readily implemented and used to implement simulation algorithms.</span></span>

<span data-ttu-id="4738a-106">Elemente in der Menge werden von einem indiziert  <xref:microsoft.quantum.simulation.generatorindex> , und jeder Satz wird von einer Funktion von `GeneratorIndex` bis beschrieben  <xref:microsoft.quantum.simulation.evolutionunitary> , die Vorgänge parametrisiert durch eine reelle Zahl, die die Zeit darstellt</span><span class="sxs-lookup"><span data-stu-id="4738a-106">Elements in the set are indexed by a  <xref:microsoft.quantum.simulation.generatorindex>, and each set is described by a function from `GeneratorIndex` to  <xref:microsoft.quantum.simulation.evolutionunitary>, which are operations parameterized by a real number representing time</span></span>

```qsharp

newtype EvolutionSet = ((Microsoft.Quantum.Simulation.GeneratorIndex -> Microsoft.Quantum.Simulation.EvolutionUnitary));
```


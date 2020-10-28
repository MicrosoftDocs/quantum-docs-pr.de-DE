---
uid: Microsoft.Quantum.Simulation.EvolutionSet
title: Benutzerdefinierter evolutionset-Typ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EvolutionSet
qsharp.summary: >-
  Represents a set of gates that can be readily implemented and used to implement simulation algorithms.

  Elements in the set are indexed by a  <xref:microsoft.quantum.simulation.generatorindex>, and each set is described by a function from `GeneratorIndex` to  <xref:microsoft.quantum.simulation.evolutionunitary>, which are operations parameterized by a real number representing time
ms.openlocfilehash: 41504837b281b1021a2d09ef75acc10315b4fd07
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701742"
---
# <a name="evolutionset-user-defined-type"></a><span data-ttu-id="b99b4-102">Benutzerdefinierter evolutionset-Typ</span><span class="sxs-lookup"><span data-stu-id="b99b4-102">EvolutionSet user defined type</span></span>

<span data-ttu-id="b99b4-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="b99b4-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="b99b4-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b99b4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b99b4-105">Stellt einen Satz von Gates dar, der leicht implementiert und zum Implementieren von Simulations Algorithmen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b99b4-105">Represents a set of gates that can be readily implemented and used to implement simulation algorithms.</span></span>

<span data-ttu-id="b99b4-106">Elemente in der Menge werden von einem indiziert  <xref:microsoft.quantum.simulation.generatorindex> , und jeder Satz wird von einer Funktion von `GeneratorIndex` bis beschrieben  <xref:microsoft.quantum.simulation.evolutionunitary> , die Vorgänge parametrisiert durch eine reelle Zahl, die die Zeit darstellt</span><span class="sxs-lookup"><span data-stu-id="b99b4-106">Elements in the set are indexed by a  <xref:microsoft.quantum.simulation.generatorindex>, and each set is described by a function from `GeneratorIndex` to  <xref:microsoft.quantum.simulation.evolutionunitary>, which are operations parameterized by a real number representing time</span></span>

```qsharp

newtype EvolutionSet = ((Microsoft.Quantum.Simulation.GeneratorIndex -> Microsoft.Quantum.Simulation.EvolutionUnitary));
```


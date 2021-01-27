---
uid: Microsoft.Quantum.Simulation.EvolutionSet
title: Benutzerdefinierter evolutionset-Typ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EvolutionSet
qsharp.summary: >-
  Represents a set of gates that can be readily implemented and used to implement simulation algorithms.

  Elements in the set are indexed by a  <xref:microsoft.quantum.simulation.generatorindex>, and each set is described by a function from `GeneratorIndex` to  <xref:microsoft.quantum.simulation.evolutionunitary>, which are operations parameterized by a real number representing time
ms.openlocfilehash: 35c0b24da284a5871fd11b6d624102b853b89d19
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856067"
---
# <a name="evolutionset-user-defined-type"></a><span data-ttu-id="e2369-102">Benutzerdefinierter evolutionset-Typ</span><span class="sxs-lookup"><span data-stu-id="e2369-102">EvolutionSet user defined type</span></span>

<span data-ttu-id="e2369-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="e2369-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="e2369-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e2369-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e2369-105">Stellt einen Satz von Gates dar, der leicht implementiert und zum Implementieren von Simulations Algorithmen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="e2369-105">Represents a set of gates that can be readily implemented and used to implement simulation algorithms.</span></span>

<span data-ttu-id="e2369-106">Elemente in der Menge werden von einem indiziert  <xref:microsoft.quantum.simulation.generatorindex> , und jeder Satz wird von einer Funktion von `GeneratorIndex` bis beschrieben  <xref:microsoft.quantum.simulation.evolutionunitary> , die Vorgänge parametrisiert durch eine reelle Zahl, die die Zeit darstellt</span><span class="sxs-lookup"><span data-stu-id="e2369-106">Elements in the set are indexed by a  <xref:microsoft.quantum.simulation.generatorindex>, and each set is described by a function from `GeneratorIndex` to  <xref:microsoft.quantum.simulation.evolutionunitary>, which are operations parameterized by a real number representing time</span></span>

```qsharp

newtype EvolutionSet = ((Microsoft.Quantum.Simulation.GeneratorIndex -> Microsoft.Quantum.Simulation.EvolutionUnitary));
```


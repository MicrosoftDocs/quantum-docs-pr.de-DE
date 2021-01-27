---
uid: Microsoft.Quantum.Simulation.EvolutionGenerator
title: Benutzerdefinierter evolutiongenerator-Typ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EvolutionGenerator
qsharp.summary: >-
  Represents a dynamical generator as a set of simulatable gates and an expansion in terms of that basis.

  Last parameter for number of terms.
ms.openlocfilehash: 98241f77bfbd73929896bb114fad060001016a86
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856088"
---
# <a name="evolutiongenerator-user-defined-type"></a><span data-ttu-id="30617-102">Benutzerdefinierter evolutiongenerator-Typ</span><span class="sxs-lookup"><span data-stu-id="30617-102">EvolutionGenerator user defined type</span></span>

<span data-ttu-id="30617-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="30617-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="30617-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="30617-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="30617-105">Stellt einen dynamischen Generator als Satz von simulier baren Gates und eine Erweiterung in Bezug auf diese Grundlage dar.</span><span class="sxs-lookup"><span data-stu-id="30617-105">Represents a dynamical generator as a set of simulatable gates and an expansion in terms of that basis.</span></span>

<span data-ttu-id="30617-106">Der letzte Parameter für die Anzahl von Begriffen.</span><span class="sxs-lookup"><span data-stu-id="30617-106">Last parameter for number of terms.</span></span>

```qsharp

newtype EvolutionGenerator = (Microsoft.Quantum.Simulation.EvolutionSet, Microsoft.Quantum.Simulation.GeneratorSystem);
```


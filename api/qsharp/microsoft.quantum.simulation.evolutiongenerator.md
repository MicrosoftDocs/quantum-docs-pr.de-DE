---
uid: Microsoft.Quantum.Simulation.EvolutionGenerator
title: Benutzerdefinierter evolutiongenerator-Typ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EvolutionGenerator
qsharp.summary: >-
  Represents a dynamical generator as a set of simulatable gates and an expansion in terms of that basis.

  Last parameter for number of terms.
ms.openlocfilehash: be741216bf99305bf5f1d149c815e98aba36aad1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701753"
---
# <a name="evolutiongenerator-user-defined-type"></a>Benutzerdefinierter evolutiongenerator-Typ

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paketen [](https://nuget.org/packages/)


Stellt einen dynamischen Generator als Satz von simulier baren Gates und eine Erweiterung in Bezug auf diese Grundlage dar.

Der letzte Parameter für die Anzahl von Begriffen.

```qsharp

newtype EvolutionGenerator = (Microsoft.Quantum.Simulation.EvolutionSet, Microsoft.Quantum.Simulation.GeneratorSystem);
```


---
uid: Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem
title: Benutzerdefinierter timedependentgeneratorsystem-Typ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TimeDependentGeneratorSystem
qsharp.summary: Represents a time-dependent dynamical generator as a function from time to the value of the dynamical generator at that time.
ms.openlocfilehash: 144a44448c9fda7a038b17ac7c49f63e8cc4dd55
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706447"
---
# <a name="timedependentgeneratorsystem-user-defined-type"></a>Benutzerdefinierter timedependentgeneratorsystem-Typ

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paketen [](https://nuget.org/packages/)


Stellt einen zeitabhängigen dynamikalischen Generator als Funktion von Time bis zum Wert des dynamischen Generators zu diesem Zeitpunkt dar.

```qsharp

newtype TimeDependentGeneratorSystem = ((Double -> Microsoft.Quantum.Simulation.GeneratorSystem));
```


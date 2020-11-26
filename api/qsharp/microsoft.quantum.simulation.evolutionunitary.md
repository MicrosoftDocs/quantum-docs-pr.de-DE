---
uid: Microsoft.Quantum.Simulation.EvolutionUnitary
title: Benutzerdefinierter evolutioneinheitlicher Typ
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EvolutionUnitary
qsharp.summary: >-
  Represents a unitary time-evolution operator.

  The first parameter is is duration of time-evolution, and the second parameter is the qubit register acted upon by the unitary.
ms.openlocfilehash: 38e7da28d4146df9cc132ad69ee939c44bc917f7
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225260"
---
# <a name="evolutionunitary-user-defined-type"></a>Benutzerdefinierter evolutioneinheitlicher Typ

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Stellt einen einheitlichen Time-Evolution-Operator dar.

Der erste Parameter ist die Dauer der Zeit-Evolution, und der zweite Parameter ist das Qubit-Register, auf das durch die einheitliche-Aktion reagiert wird.

```qsharp

newtype EvolutionUnitary = (((Double, Qubit[]) => Unit is Adj + Ctl));
```


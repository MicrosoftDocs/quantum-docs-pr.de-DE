---
uid: Microsoft.Quantum.Simulation.Unitary
title: Einheitlicher benutzerdefinierter Typ
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: Unitary
qsharp.summary: Represents evolution under a unitary operator.
ms.openlocfilehash: c34d84fb5f319c285356b284bd1f1c18ec64ef46
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192144"
---
# <a name="unitary-user-defined-type"></a>Einheitlicher benutzerdefinierter Typ

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Stellt die Weiterentwicklung unter einem einheitlichen Operator dar.

```qsharp

newtype Unitary = ((Qubit[] => Unit is Adj + Ctl));
```


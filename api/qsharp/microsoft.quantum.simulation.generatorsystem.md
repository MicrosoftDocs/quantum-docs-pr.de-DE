---
uid: Microsoft.Quantum.Simulation.GeneratorSystem
title: Benutzerdefinierter Generatorsystem-Typ
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: GeneratorSystem
qsharp.summary: >-
  Represents a collection of `GeneratorIndex`es.

  We iterate over this collection using a single-index integer, and the size of the collection is assumed to be known.
ms.openlocfilehash: 20092a8deca50c90f46f4d79c6b40b805f135754
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225226"
---
# <a name="generatorsystem-user-defined-type"></a>Benutzerdefinierter Generatorsystem-Typ

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Stellt eine Auflistung von `GeneratorIndex` es dar.

Wir durchlaufen diese Auflistung mit einer Einzel Index-Ganzzahl, und es wird davon ausgegangen, dass die Größe der Auflistung bekannt ist.

```qsharp

newtype GeneratorSystem = (Int, (Int -> Microsoft.Quantum.Simulation.GeneratorIndex));
```



## <a name="remarks"></a>Bemerkungen

Instanzen von `GeneratorSystem` können problemlos mithilfe der-Funktion definiert werden <xref:microsoft.quantum.arrays.lookupfunction> .

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Arrays. lookupfunction](xref:Microsoft.Quantum.Arrays.LookupFunction)
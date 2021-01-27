---
uid: Microsoft.Quantum.Simulation.GeneratorSystem
title: Benutzerdefinierter Generatorsystem-Typ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: GeneratorSystem
qsharp.summary: >-
  Represents a collection of `GeneratorIndex`es.

  We iterate over this collection using a single-index integer, and the size of the collection is assumed to be known.
ms.openlocfilehash: 3748d3fb79597fb526c86a91bc28290155189014
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858407"
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
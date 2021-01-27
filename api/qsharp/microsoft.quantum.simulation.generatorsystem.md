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
# <a name="generatorsystem-user-defined-type"></a><span data-ttu-id="06a13-102">Benutzerdefinierter Generatorsystem-Typ</span><span class="sxs-lookup"><span data-stu-id="06a13-102">GeneratorSystem user defined type</span></span>

<span data-ttu-id="06a13-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="06a13-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="06a13-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="06a13-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="06a13-105">Stellt eine Auflistung von `GeneratorIndex` es dar.</span><span class="sxs-lookup"><span data-stu-id="06a13-105">Represents a collection of `GeneratorIndex`es.</span></span>

<span data-ttu-id="06a13-106">Wir durchlaufen diese Auflistung mit einer Einzel Index-Ganzzahl, und es wird davon ausgegangen, dass die Größe der Auflistung bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="06a13-106">We iterate over this collection using a single-index integer, and the size of the collection is assumed to be known.</span></span>

```qsharp

newtype GeneratorSystem = (Int, (Int -> Microsoft.Quantum.Simulation.GeneratorIndex));
```



## <a name="remarks"></a><span data-ttu-id="06a13-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="06a13-107">Remarks</span></span>

<span data-ttu-id="06a13-108">Instanzen von `GeneratorSystem` können problemlos mithilfe der-Funktion definiert werden <xref:microsoft.quantum.arrays.lookupfunction> .</span><span class="sxs-lookup"><span data-stu-id="06a13-108">Instances of `GeneratorSystem` can be defined easily using the <xref:microsoft.quantum.arrays.lookupfunction> function.</span></span>

## <a name="see-also"></a><span data-ttu-id="06a13-109">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="06a13-109">See Also</span></span>

- [<span data-ttu-id="06a13-110">Microsoft. Quantum. Arrays. lookupfunction</span><span class="sxs-lookup"><span data-stu-id="06a13-110">Microsoft.Quantum.Arrays.LookupFunction</span></span>](xref:Microsoft.Quantum.Arrays.LookupFunction)
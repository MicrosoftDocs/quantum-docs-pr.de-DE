---
uid: Microsoft.Quantum.Simulation.GeneratorSystem
title: Benutzerdefinierter Generatorsystem-Typ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: GeneratorSystem
qsharp.summary: >-
  Represents a collection of `GeneratorIndex`es.

  We iterate over this collection using a single-index integer, and the size of the collection is assumed to be known.
ms.openlocfilehash: c03caf99b197410c7fa15021c8acaaf55a728781
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724558"
---
# <a name="generatorsystem-user-defined-type"></a><span data-ttu-id="7c95a-102">Benutzerdefinierter Generatorsystem-Typ</span><span class="sxs-lookup"><span data-stu-id="7c95a-102">GeneratorSystem user defined type</span></span>

<span data-ttu-id="7c95a-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="7c95a-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="7c95a-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7c95a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7c95a-105">Stellt eine Auflistung von `GeneratorIndex` es dar.</span><span class="sxs-lookup"><span data-stu-id="7c95a-105">Represents a collection of `GeneratorIndex`es.</span></span>

<span data-ttu-id="7c95a-106">Wir durchlaufen diese Auflistung mit einer Einzel Index-Ganzzahl, und es wird davon ausgegangen, dass die Größe der Auflistung bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="7c95a-106">We iterate over this collection using a single-index integer, and the size of the collection is assumed to be known.</span></span>

```qsharp

newtype GeneratorSystem = (Int, (Int -> Microsoft.Quantum.Simulation.GeneratorIndex));
```



## <a name="remarks"></a><span data-ttu-id="7c95a-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7c95a-107">Remarks</span></span>

<span data-ttu-id="7c95a-108">Instanzen von `GeneratorSystem` können problemlos mithilfe der-Funktion definiert werden <xref:microsoft.quantum.arrays.lookupfunction> .</span><span class="sxs-lookup"><span data-stu-id="7c95a-108">Instances of `GeneratorSystem` can be defined easily using the <xref:microsoft.quantum.arrays.lookupfunction> function.</span></span>

## <a name="see-also"></a><span data-ttu-id="7c95a-109">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7c95a-109">See Also</span></span>

- [<span data-ttu-id="7c95a-110">Microsoft. Quantum. Arrays. lookupfunction</span><span class="sxs-lookup"><span data-stu-id="7c95a-110">Microsoft.Quantum.Arrays.LookupFunction</span></span>](xref:Microsoft.Quantum.Arrays.LookupFunction)
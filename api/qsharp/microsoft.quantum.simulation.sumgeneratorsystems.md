---
uid: Microsoft.Quantum.Simulation.SumGeneratorSystems
title: Sumgeneratorsystems-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: SumGeneratorSystems
qsharp.summary: Adds multiple `GeneratorSystem`s to create a new GeneratorSystem.
ms.openlocfilehash: 0e64d2b599c55c19711208670030fd01e09aff7e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851020"
---
# <a name="sumgeneratorsystems-function"></a><span data-ttu-id="f6a81-102">Sumgeneratorsystems-Funktion</span><span class="sxs-lookup"><span data-stu-id="f6a81-102">SumGeneratorSystems function</span></span>

<span data-ttu-id="f6a81-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="f6a81-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="f6a81-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f6a81-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f6a81-105">Fügt mehrere `GeneratorSystem` s hinzu, um ein neues Generatorsystem zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f6a81-105">Adds multiple `GeneratorSystem`s to create a new GeneratorSystem.</span></span>

```qsharp
function SumGeneratorSystems (generatorSystems : Microsoft.Quantum.Simulation.GeneratorSystem[]) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a><span data-ttu-id="f6a81-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f6a81-106">Input</span></span>

### <a name="generatorsystems--generatorsystem"></a><span data-ttu-id="f6a81-107">Generatorsystems: [Generatorsystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)[]</span><span class="sxs-lookup"><span data-stu-id="f6a81-107">generatorSystems : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)[]</span></span>

<span data-ttu-id="f6a81-108">Ein Array vom Typ `GeneratorSystem[]`.</span><span class="sxs-lookup"><span data-stu-id="f6a81-108">An array of type `GeneratorSystem[]`.</span></span>



## <a name="output--generatorsystem"></a><span data-ttu-id="f6a81-109">Ausgabe: [Generatorsystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="f6a81-109">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="f6a81-110">Ein `GeneratorSystem` , das ein System darstellt, das die Summe der Eingabe Generator Systeme darstellt.</span><span class="sxs-lookup"><span data-stu-id="f6a81-110">A `GeneratorSystem` representing a system that is the sum of the input generator systems.</span></span>

## <a name="see-also"></a><span data-ttu-id="f6a81-111">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f6a81-111">See Also</span></span>

- [<span data-ttu-id="f6a81-112">Microsoft. Quantum. Simulation. Generatorsystem</span><span class="sxs-lookup"><span data-stu-id="f6a81-112">Microsoft.Quantum.Simulation.GeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorSystem)
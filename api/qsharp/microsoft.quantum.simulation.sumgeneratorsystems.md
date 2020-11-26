---
uid: Microsoft.Quantum.Simulation.SumGeneratorSystems
title: Sumgeneratorsystems-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: SumGeneratorSystems
qsharp.summary: Adds multiple `GeneratorSystem`s to create a new GeneratorSystem.
ms.openlocfilehash: 7cb18e161dce3a52d7c9a0bf6a45d4818db2b849
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192467"
---
# <a name="sumgeneratorsystems-function"></a><span data-ttu-id="d263f-102">Sumgeneratorsystems-Funktion</span><span class="sxs-lookup"><span data-stu-id="d263f-102">SumGeneratorSystems function</span></span>

<span data-ttu-id="d263f-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="d263f-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="d263f-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d263f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d263f-105">Fügt mehrere `GeneratorSystem` s hinzu, um ein neues Generatorsystem zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d263f-105">Adds multiple `GeneratorSystem`s to create a new GeneratorSystem.</span></span>

```qsharp
function SumGeneratorSystems (generatorSystems : Microsoft.Quantum.Simulation.GeneratorSystem[]) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a><span data-ttu-id="d263f-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d263f-106">Input</span></span>

### <a name="generatorsystems--generatorsystem"></a><span data-ttu-id="d263f-107">Generatorsystems: [Generatorsystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)[]</span><span class="sxs-lookup"><span data-stu-id="d263f-107">generatorSystems : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)[]</span></span>

<span data-ttu-id="d263f-108">Ein Array vom Typ `GeneratorSystem[]`.</span><span class="sxs-lookup"><span data-stu-id="d263f-108">An array of type `GeneratorSystem[]`.</span></span>



## <a name="output--generatorsystem"></a><span data-ttu-id="d263f-109">Ausgabe: [Generatorsystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="d263f-109">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="d263f-110">Ein `GeneratorSystem` , das ein System darstellt, das die Summe der Eingabe Generator Systeme darstellt.</span><span class="sxs-lookup"><span data-stu-id="d263f-110">A `GeneratorSystem` representing a system that is the sum of the input generator systems.</span></span>

## <a name="see-also"></a><span data-ttu-id="d263f-111">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d263f-111">See Also</span></span>

- [<span data-ttu-id="d263f-112">Microsoft. Quantum. Simulation. Generatorsystem</span><span class="sxs-lookup"><span data-stu-id="d263f-112">Microsoft.Quantum.Simulation.GeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorSystem)
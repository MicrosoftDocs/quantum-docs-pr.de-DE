---
uid: Microsoft.Quantum.MachineLearning.CombinedStructure
title: Combinedstructure-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: CombinedStructure
qsharp.summary: Given one or more layers of controlled rotations, returns a single layer with model parameter index shifted such that distinct layers are parameterized by distinct model parameters.
ms.openlocfilehash: 0a7d66be8b45d6a9df95b425e66b9b6bba241136
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211966"
---
# <a name="combinedstructure-function"></a><span data-ttu-id="33f49-102">Combinedstructure-Funktion</span><span class="sxs-lookup"><span data-stu-id="33f49-102">CombinedStructure function</span></span>

<span data-ttu-id="33f49-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="33f49-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="33f49-104">Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="33f49-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="33f49-105">Bei einer oder mehreren Ebenen kontrollierter Drehungen gibt eine einzelne Ebene zurück, bei der der Modellparameter Index so verschoben wurde, dass unterschiedliche Ebenen von unterschiedlichen Modellparametern parametrisiert werden.</span><span class="sxs-lookup"><span data-stu-id="33f49-105">Given one or more layers of controlled rotations, returns a single layer with model parameter index shifted such that distinct layers are parameterized by distinct model parameters.</span></span>

```qsharp
function CombinedStructure (layers : Microsoft.Quantum.MachineLearning.ControlledRotation[][]) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a><span data-ttu-id="33f49-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="33f49-106">Input</span></span>

### <a name="layers--controlledrotation"></a><span data-ttu-id="33f49-107">Ebenen: [controlledrotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[] []</span><span class="sxs-lookup"><span data-stu-id="33f49-107">layers : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[][]</span></span>

<span data-ttu-id="33f49-108">Die zu kombinierenden Ebenen.</span><span class="sxs-lookup"><span data-stu-id="33f49-108">The layers to be combined.</span></span>



## <a name="output--controlledrotation"></a><span data-ttu-id="33f49-109">Ausgabe: [controlledrotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span><span class="sxs-lookup"><span data-stu-id="33f49-109">Output : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span></span>

<span data-ttu-id="33f49-110">Eine einzelne Ebene von kontrollierten Rotationen, die die Verkettung aller anderen Ebenen darstellt.</span><span class="sxs-lookup"><span data-stu-id="33f49-110">A single layer of controlled rotations, representing the concatenation of all other layers.</span></span>
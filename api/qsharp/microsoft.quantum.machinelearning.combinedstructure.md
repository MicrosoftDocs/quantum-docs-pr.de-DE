---
uid: Microsoft.Quantum.MachineLearning.CombinedStructure
title: Combinedstructure-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: CombinedStructure
qsharp.summary: Given one or more layers of controlled rotations, returns a single layer with model parameter index shifted such that distinct layers are parameterized by distinct model parameters.
ms.openlocfilehash: fbfd87761a40abe350e5f955fb53d8024eeb614e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706874"
---
# <a name="combinedstructure-function"></a><span data-ttu-id="ad6bf-102">Combinedstructure-Funktion</span><span class="sxs-lookup"><span data-stu-id="ad6bf-102">CombinedStructure function</span></span>

<span data-ttu-id="ad6bf-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="ad6bf-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="ad6bf-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ad6bf-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ad6bf-105">Bei einer oder mehreren Ebenen kontrollierter Drehungen gibt eine einzelne Ebene zurück, bei der der Modellparameter Index so verschoben wurde, dass unterschiedliche Ebenen von unterschiedlichen Modellparametern parametrisiert werden.</span><span class="sxs-lookup"><span data-stu-id="ad6bf-105">Given one or more layers of controlled rotations, returns a single layer with model parameter index shifted such that distinct layers are parameterized by distinct model parameters.</span></span>

```qsharp
function CombinedStructure (layers : Microsoft.Quantum.MachineLearning.ControlledRotation[][]) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a><span data-ttu-id="ad6bf-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ad6bf-106">Input</span></span>

### <a name="layers--controlledrotation"></a><span data-ttu-id="ad6bf-107">Ebenen: [controlledrotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[] []</span><span class="sxs-lookup"><span data-stu-id="ad6bf-107">layers : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[][]</span></span>

<span data-ttu-id="ad6bf-108">Die zu kombinierenden Ebenen.</span><span class="sxs-lookup"><span data-stu-id="ad6bf-108">The layers to be combined.</span></span>



## <a name="output--controlledrotation"></a><span data-ttu-id="ad6bf-109">Ausgabe: [controlledrotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span><span class="sxs-lookup"><span data-stu-id="ad6bf-109">Output : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span></span>

<span data-ttu-id="ad6bf-110">Eine einzelne Ebene von kontrollierten Rotationen, die die Verkettung aller anderen Ebenen darstellt.</span><span class="sxs-lookup"><span data-stu-id="ad6bf-110">A single layer of controlled rotations, representing the concatenation of all other layers.</span></span>
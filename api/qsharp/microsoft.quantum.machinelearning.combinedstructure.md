---
uid: Microsoft.Quantum.MachineLearning.CombinedStructure
title: Combinedstructure-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: CombinedStructure
qsharp.summary: Given one or more layers of controlled rotations, returns a single layer with model parameter index shifted such that distinct layers are parameterized by distinct model parameters.
ms.openlocfilehash: b8ec007202c8e63dc2e98d0c752f6ba1a453e236
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847420"
---
# <a name="combinedstructure-function"></a><span data-ttu-id="3c149-102">Combinedstructure-Funktion</span><span class="sxs-lookup"><span data-stu-id="3c149-102">CombinedStructure function</span></span>

<span data-ttu-id="3c149-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="3c149-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="3c149-104">Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="3c149-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="3c149-105">Bei einer oder mehreren Ebenen kontrollierter Drehungen gibt eine einzelne Ebene zurück, bei der der Modellparameter Index so verschoben wurde, dass unterschiedliche Ebenen von unterschiedlichen Modellparametern parametrisiert werden.</span><span class="sxs-lookup"><span data-stu-id="3c149-105">Given one or more layers of controlled rotations, returns a single layer with model parameter index shifted such that distinct layers are parameterized by distinct model parameters.</span></span>

```qsharp
function CombinedStructure (layers : Microsoft.Quantum.MachineLearning.ControlledRotation[][]) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a><span data-ttu-id="3c149-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3c149-106">Input</span></span>

### <a name="layers--controlledrotation"></a><span data-ttu-id="3c149-107">Ebenen: [controlledrotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[] []</span><span class="sxs-lookup"><span data-stu-id="3c149-107">layers : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[][]</span></span>

<span data-ttu-id="3c149-108">Die zu kombinierenden Ebenen.</span><span class="sxs-lookup"><span data-stu-id="3c149-108">The layers to be combined.</span></span>



## <a name="output--controlledrotation"></a><span data-ttu-id="3c149-109">Ausgabe: [controlledrotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span><span class="sxs-lookup"><span data-stu-id="3c149-109">Output : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span></span>

<span data-ttu-id="3c149-110">Eine einzelne Ebene von kontrollierten Rotationen, die die Verkettung aller anderen Ebenen darstellt.</span><span class="sxs-lookup"><span data-stu-id="3c149-110">A single layer of controlled rotations, representing the concatenation of all other layers.</span></span>

## <a name="example"></a><span data-ttu-id="3c149-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3c149-111">Example</span></span>

<span data-ttu-id="3c149-112">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="3c149-112">The following are equivalent:</span></span>

```qsharp
let structure = CombinedStructure([
    LocalRotationLayer(2, PauliY),
    CyclicEntanglingLayer(3, PauliX, 2)
]);
let structure = [
    ControlledRotation((0, new Int[0]), PauliY, 0),
    ControlledRotation((1, new Int[0]), PauliY, 1),
    ControlledRotation((0, [2]), PauliX, 2),
    ControlledRotation((1, [0]), PauliX, 3),
    ControlledRotation((2, [1]), PauliX, 4)
];
```
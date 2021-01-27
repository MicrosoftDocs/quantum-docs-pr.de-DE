---
uid: Microsoft.Quantum.MachineLearning.SequentialModel
title: Sequentialmodel-benutzerdefinierter Typ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: SequentialModel
qsharp.summary: Describes a quantum classifier model composed of a sequence of parameterized and controlled rotations, an assignment of rotation angles, and a bias between the two classes recognized by the model.
ms.openlocfilehash: ab9c121884e489b5d056285008c91c1ad70bb053
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854894"
---
# <a name="sequentialmodel-user-defined-type"></a><span data-ttu-id="ca6ab-102">Sequentialmodel-benutzerdefinierter Typ</span><span class="sxs-lookup"><span data-stu-id="ca6ab-102">SequentialModel user defined type</span></span>

<span data-ttu-id="ca6ab-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="ca6ab-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="ca6ab-104">Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="ca6ab-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="ca6ab-105">Beschreibt ein Quantum Klassifizierungs-Modell, das aus einer Sequenz von parametrisierten und kontrollierten Drehungen, einer Zuweisung von Drehwinkeln und einer Abweichung zwischen den beiden vom Modell erkannten Klassen besteht.</span><span class="sxs-lookup"><span data-stu-id="ca6ab-105">Describes a quantum classifier model composed of a sequence of parameterized and controlled rotations, an assignment of rotation angles, and a bias between the two classes recognized by the model.</span></span>

```qsharp

newtype SequentialModel = (Structure : Microsoft.Quantum.MachineLearning.ControlledRotation[], Parameters : Double[], Bias : Double);
```



## <a name="named-items"></a><span data-ttu-id="ca6ab-106">Benannte Elemente</span><span class="sxs-lookup"><span data-stu-id="ca6ab-106">Named Items</span></span>

### <a name="structure--controlledrotation"></a><span data-ttu-id="ca6ab-107">Struktur: [controlledrotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span><span class="sxs-lookup"><span data-stu-id="ca6ab-107">Structure : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span></span>

<span data-ttu-id="ca6ab-108">Die Sequenz der kontrollierten Drehungen, die zum Klassifizieren von Eingaben verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ca6ab-108">The sequence of controlled rotations used to classify inputs.</span></span>
### <a name="parameters--double"></a><span data-ttu-id="ca6ab-109">Parameter: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="ca6ab-109">Parameters : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="ca6ab-110">Eine Zuweisung der Drehwinkel zur angegebenen Klassifizierungs Struktur.</span><span class="sxs-lookup"><span data-stu-id="ca6ab-110">An assignment of rotation angles to the given classification structure.</span></span>
### <a name="bias--double"></a><span data-ttu-id="ca6ab-111">Bias: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="ca6ab-111">Bias : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="ca6ab-112">Die Abweichung zwischen den beiden Klassen, die von diesem Klassifizierer erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="ca6ab-112">The bias between the two classes recognized by this classifier.</span></span>

## <a name="references"></a><span data-ttu-id="ca6ab-113">References</span><span class="sxs-lookup"><span data-stu-id="ca6ab-113">References</span></span>

- [<span data-ttu-id="ca6ab-114">arXiv: 1804.00633</span><span class="sxs-lookup"><span data-stu-id="ca6ab-114">arXiv:1804.00633</span></span>](https://arxiv.org/abs/1804.00633)
---
uid: Microsoft.Quantum.MachineLearning.SequentialModel
title: Sequentialmodel-benutzerdefinierter Typ
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: SequentialModel
qsharp.summary: Describes a quantum classifier model composed of a sequence of parameterized and controlled rotations, an assignment of rotation angles, and a bias between the two classes recognized by the model.
ms.openlocfilehash: 3afdb8dafe0179535fe5d8c3dff668f1f3de2f7d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196173"
---
# <a name="sequentialmodel-user-defined-type"></a><span data-ttu-id="f7b30-102">Sequentialmodel-benutzerdefinierter Typ</span><span class="sxs-lookup"><span data-stu-id="f7b30-102">SequentialModel user defined type</span></span>

<span data-ttu-id="f7b30-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="f7b30-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="f7b30-104">Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="f7b30-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="f7b30-105">Beschreibt ein Quantum Klassifizierungs-Modell, das aus einer Sequenz von parametrisierten und kontrollierten Drehungen, einer Zuweisung von Drehwinkeln und einer Abweichung zwischen den beiden vom Modell erkannten Klassen besteht.</span><span class="sxs-lookup"><span data-stu-id="f7b30-105">Describes a quantum classifier model composed of a sequence of parameterized and controlled rotations, an assignment of rotation angles, and a bias between the two classes recognized by the model.</span></span>

```qsharp

newtype SequentialModel = (Structure : Microsoft.Quantum.MachineLearning.ControlledRotation[], Parameters : Double[], Bias : Double);
```



## <a name="named-items"></a><span data-ttu-id="f7b30-106">Benannte Elemente</span><span class="sxs-lookup"><span data-stu-id="f7b30-106">Named Items</span></span>

### <a name="structure--controlledrotation"></a><span data-ttu-id="f7b30-107">Struktur: [controlledrotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span><span class="sxs-lookup"><span data-stu-id="f7b30-107">Structure : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span></span>

<span data-ttu-id="f7b30-108">Die Sequenz der kontrollierten Drehungen, die zum Klassifizieren von Eingaben verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f7b30-108">The sequence of controlled rotations used to classify inputs.</span></span>
### <a name="parameters--double"></a><span data-ttu-id="f7b30-109">Parameter: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="f7b30-109">Parameters : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="f7b30-110">Eine Zuweisung der Drehwinkel zur angegebenen Klassifizierungs Struktur.</span><span class="sxs-lookup"><span data-stu-id="f7b30-110">An assignment of rotation angles to the given classification structure.</span></span>
### <a name="bias--double"></a><span data-ttu-id="f7b30-111">Bias: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="f7b30-111">Bias : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="f7b30-112">Die Abweichung zwischen den beiden Klassen, die von diesem Klassifizierer erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="f7b30-112">The bias between the two classes recognized by this classifier.</span></span>

## <a name="references"></a><span data-ttu-id="f7b30-113">Referenzen</span><span class="sxs-lookup"><span data-stu-id="f7b30-113">References</span></span>

- [<span data-ttu-id="f7b30-114">arXiv: 1804.00633</span><span class="sxs-lookup"><span data-stu-id="f7b30-114">arXiv:1804.00633</span></span>](https://arxiv.org/abs/1804.00633)
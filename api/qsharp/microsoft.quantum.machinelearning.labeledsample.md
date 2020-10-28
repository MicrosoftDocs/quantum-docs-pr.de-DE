---
uid: Microsoft.Quantum.MachineLearning.LabeledSample
title: Benutzerdefinierter Typ "labeledsample"
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: LabeledSample
qsharp.summary: A sample, labeled with a class to which that sample belongs.
ms.openlocfilehash: 8b4afa1eaf7ca69938b2606163cd1ec17a1ad80f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702053"
---
# <a name="labeledsample-user-defined-type"></a><span data-ttu-id="c214e-102">Benutzerdefinierter Typ "labeledsample"</span><span class="sxs-lookup"><span data-stu-id="c214e-102">LabeledSample user defined type</span></span>

<span data-ttu-id="c214e-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="c214e-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="c214e-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c214e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c214e-105">Ein Beispiel mit einer Klasse, zu der das Beispiel gehört.</span><span class="sxs-lookup"><span data-stu-id="c214e-105">A sample, labeled with a class to which that sample belongs.</span></span>

```qsharp

newtype LabeledSample = (Features : Double[], Label : Int);
```



## <a name="named-items"></a><span data-ttu-id="c214e-106">Benannte Elemente</span><span class="sxs-lookup"><span data-stu-id="c214e-106">Named Items</span></span>

### <a name="features--double"></a><span data-ttu-id="c214e-107">Features: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="c214e-107">Features : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="c214e-108">Ein Vektor von Features für das angegebene Beispiel.</span><span class="sxs-lookup"><span data-stu-id="c214e-108">A vector of features for the given sample.</span></span>
### <a name="label--int"></a><span data-ttu-id="c214e-109">Bezeichnung: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c214e-109">Label : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c214e-110">Eine ganzzahlige Bezeichnung für die Klasse, zu der dieses Beispiel gehört.</span><span class="sxs-lookup"><span data-stu-id="c214e-110">An integer label for the class to which this sample belongs.</span></span>
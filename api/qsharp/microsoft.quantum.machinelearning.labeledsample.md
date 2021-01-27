---
uid: Microsoft.Quantum.MachineLearning.LabeledSample
title: Benutzerdefinierter Typ "labeledsample"
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: LabeledSample
qsharp.summary: A sample, labeled with a class to which that sample belongs.
ms.openlocfilehash: b357aae20b5bddb968ce1906fed3c1001efbfde7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846981"
---
# <a name="labeledsample-user-defined-type"></a><span data-ttu-id="a07d6-102">Benutzerdefinierter Typ "labeledsample"</span><span class="sxs-lookup"><span data-stu-id="a07d6-102">LabeledSample user defined type</span></span>

<span data-ttu-id="a07d6-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="a07d6-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="a07d6-104">Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="a07d6-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="a07d6-105">Ein Beispiel mit einer Klasse, zu der das Beispiel gehört.</span><span class="sxs-lookup"><span data-stu-id="a07d6-105">A sample, labeled with a class to which that sample belongs.</span></span>

```qsharp

newtype LabeledSample = (Features : Double[], Label : Int);
```



## <a name="named-items"></a><span data-ttu-id="a07d6-106">Benannte Elemente</span><span class="sxs-lookup"><span data-stu-id="a07d6-106">Named Items</span></span>

### <a name="features--double"></a><span data-ttu-id="a07d6-107">Features: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="a07d6-107">Features : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="a07d6-108">Ein Vektor von Features für das angegebene Beispiel.</span><span class="sxs-lookup"><span data-stu-id="a07d6-108">A vector of features for the given sample.</span></span>
### <a name="label--int"></a><span data-ttu-id="a07d6-109">Bezeichnung: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a07d6-109">Label : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a07d6-110">Eine ganzzahlige Bezeichnung für die Klasse, zu der dieses Beispiel gehört.</span><span class="sxs-lookup"><span data-stu-id="a07d6-110">An integer label for the class to which this sample belongs.</span></span>
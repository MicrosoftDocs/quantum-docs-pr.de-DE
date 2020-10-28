---
uid: Microsoft.Quantum.MachineLearning.ValidationResults
title: Benutzerdefinierter ValidationResults-Typ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ValidationResults
qsharp.summary: The results from having validated a classifier against a set of samples.
ms.openlocfilehash: 1e54a5a086035f5f8d36d777badb306156d99600
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706815"
---
# <a name="validationresults-user-defined-type"></a><span data-ttu-id="e6f77-102">Benutzerdefinierter ValidationResults-Typ</span><span class="sxs-lookup"><span data-stu-id="e6f77-102">ValidationResults user defined type</span></span>

<span data-ttu-id="e6f77-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="e6f77-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="e6f77-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e6f77-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e6f77-105">Die Ergebnisse aus der Validierung eines Klassifizierers mit einer Reihe von Beispielen.</span><span class="sxs-lookup"><span data-stu-id="e6f77-105">The results from having validated a classifier against a set of samples.</span></span>

```qsharp

newtype ValidationResults = (NMisclassifications : Int, NValidationSamples : Int);
```



## <a name="named-items"></a><span data-ttu-id="e6f77-106">Benannte Elemente</span><span class="sxs-lookup"><span data-stu-id="e6f77-106">Named Items</span></span>

### <a name="nmisclassifications--int"></a><span data-ttu-id="e6f77-107">Nfehlklassifizierungen: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e6f77-107">NMisclassifications : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e6f77-108">Die Anzahl der während der Validierung beobachteten fehl Klassifizierungen.</span><span class="sxs-lookup"><span data-stu-id="e6f77-108">The number of misclassifications observed during validation.</span></span>
### <a name="nvalidationsamples--int"></a><span data-ttu-id="e6f77-109">Nvalidationsamples: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e6f77-109">NValidationSamples : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>


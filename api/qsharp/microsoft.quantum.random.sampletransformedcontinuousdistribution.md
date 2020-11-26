---
uid: Microsoft.Quantum.Random.SampleTransformedContinuousDistribution
title: Sampletransformedcontinuousdistribution-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: SampleTransformedContinuousDistribution
qsharp.summary: Internal-only operation for sampling from transformed distributions. Should only be used via partial application.
ms.openlocfilehash: f9f2b3cbbb4423f267758976cd066abbfec93a77
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192688"
---
# <a name="sampletransformedcontinuousdistribution-operation"></a><span data-ttu-id="7ad7c-102">Sampletransformedcontinuousdistribution-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7ad7c-102">SampleTransformedContinuousDistribution operation</span></span>

<span data-ttu-id="7ad7c-103">Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="7ad7c-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="7ad7c-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="7ad7c-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="7ad7c-105">Interner Vorgang für die Stichprobenentnahme aus transformierten Verteilungen.</span><span class="sxs-lookup"><span data-stu-id="7ad7c-105">Internal-only operation for sampling from transformed distributions.</span></span>
<span data-ttu-id="7ad7c-106">Sollte nur über eine partielle Anwendung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7ad7c-106">Should only be used via partial application.</span></span>

```qsharp
operation SampleTransformedContinuousDistribution (transform : (Double -> Double), distribution : Microsoft.Quantum.Random.ContinuousDistribution) : Double
```


## <a name="input"></a><span data-ttu-id="7ad7c-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7ad7c-107">Input</span></span>

### <a name="transform--double---double"></a><span data-ttu-id="7ad7c-108">Transformation: [Double](xref:microsoft.quantum.lang-ref.double) -> [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="7ad7c-108">transform : [Double](xref:microsoft.quantum.lang-ref.double) -> [Double](xref:microsoft.quantum.lang-ref.double)</span></span>




### <a name="distribution--continuousdistribution"></a><span data-ttu-id="7ad7c-109">Verteilung: [continuousdistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="7ad7c-109">distribution : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>





## <a name="output--double"></a><span data-ttu-id="7ad7c-110">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="7ad7c-110">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>


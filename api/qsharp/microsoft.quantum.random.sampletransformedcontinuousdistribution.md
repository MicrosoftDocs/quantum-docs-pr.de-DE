---
uid: Microsoft.Quantum.Random.SampleTransformedContinuousDistribution
title: Sampletransformedcontinuousdistribution-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: SampleTransformedContinuousDistribution
qsharp.summary: Internal-only operation for sampling from transformed distributions. Should only be used via partial application.
ms.openlocfilehash: 62f6f4ff372143228de007c98a23697022fcfd24
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856098"
---
# <a name="sampletransformedcontinuousdistribution-operation"></a><span data-ttu-id="7afdf-102">Sampletransformedcontinuousdistribution-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7afdf-102">SampleTransformedContinuousDistribution operation</span></span>

<span data-ttu-id="7afdf-103">Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="7afdf-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="7afdf-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="7afdf-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="7afdf-105">Interner Vorgang für die Stichprobenentnahme aus transformierten Verteilungen.</span><span class="sxs-lookup"><span data-stu-id="7afdf-105">Internal-only operation for sampling from transformed distributions.</span></span>
<span data-ttu-id="7afdf-106">Sollte nur über eine partielle Anwendung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7afdf-106">Should only be used via partial application.</span></span>

```qsharp
operation SampleTransformedContinuousDistribution (transform : (Double -> Double), distribution : Microsoft.Quantum.Random.ContinuousDistribution) : Double
```


## <a name="input"></a><span data-ttu-id="7afdf-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7afdf-107">Input</span></span>

### <a name="transform--double---double"></a><span data-ttu-id="7afdf-108">Transformation: [Double](xref:microsoft.quantum.lang-ref.double) -> [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="7afdf-108">transform : [Double](xref:microsoft.quantum.lang-ref.double) -> [Double](xref:microsoft.quantum.lang-ref.double)</span></span>




### <a name="distribution--continuousdistribution"></a><span data-ttu-id="7afdf-109">Verteilung: [continuousdistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="7afdf-109">distribution : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>





## <a name="output--double"></a><span data-ttu-id="7afdf-110">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="7afdf-110">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>


---
uid: Microsoft.Quantum.Random.TransformedContinuousDistribution
title: Transformedcontinuousdistribution-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: TransformedContinuousDistribution
qsharp.summary: Given a continuous distribution, returns a new distribution that transforms the original by a given function.
ms.openlocfilehash: b317eaaa0ff0180ea5d240464c96d1c6b59c9c70
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226263"
---
# <a name="transformedcontinuousdistribution-function"></a><span data-ttu-id="2befb-102">Transformedcontinuousdistribution-Funktion</span><span class="sxs-lookup"><span data-stu-id="2befb-102">TransformedContinuousDistribution function</span></span>

<span data-ttu-id="2befb-103">Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="2befb-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="2befb-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="2befb-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="2befb-105">Gibt bei einer kontinuierlichen Verteilung eine neue Verteilung zurück, die den ursprünglichen durch eine angegebene Funktion transformiert.</span><span class="sxs-lookup"><span data-stu-id="2befb-105">Given a continuous distribution, returns a new distribution that transforms the original by a given function.</span></span>

```qsharp
function TransformedContinuousDistribution (transform : (Double -> Double), distribution : Microsoft.Quantum.Random.ContinuousDistribution) : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="input"></a><span data-ttu-id="2befb-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2befb-106">Input</span></span>

### <a name="transform--double---double"></a><span data-ttu-id="2befb-107">Transformation: [Double](xref:microsoft.quantum.lang-ref.double) -> [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="2befb-107">transform : [Double](xref:microsoft.quantum.lang-ref.double) -> [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="2befb-108">Eine Funktion, die variate der ursprünglichen Verteilung in die transformierte Verteilung umwandelt.</span><span class="sxs-lookup"><span data-stu-id="2befb-108">A function that transforms variates of the original distribution to the transformed distribution.</span></span>


### <a name="distribution--continuousdistribution"></a><span data-ttu-id="2befb-109">Verteilung: [continuousdistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="2befb-109">distribution : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>

<span data-ttu-id="2befb-110">Die ursprüngliche Verteilung, die transformiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="2befb-110">The original distribution to be transformed.</span></span>



## <a name="output--continuousdistribution"></a><span data-ttu-id="2befb-111">Ausgabe: [continuousdistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="2befb-111">Output : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>

<span data-ttu-id="2befb-112">Eine neue Distribution, `distribution` die durch die durch angegebene Transformation verknüpft ist `transform` .</span><span class="sxs-lookup"><span data-stu-id="2befb-112">A new distribution related to `distribution` by the transformation given by `transform`.</span></span>
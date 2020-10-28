---
uid: Microsoft.Quantum.Random.TransformedContinuousDistribution
title: Transformedcontinuousdistribution-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: TransformedContinuousDistribution
qsharp.summary: Given a continuous distribution, returns a new distribution that transforms the original by a given function.
ms.openlocfilehash: 6a6e0c26bd650fd4c05208197ff23f951d1c3b5c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701885"
---
# <a name="transformedcontinuousdistribution-function"></a><span data-ttu-id="83e68-102">Transformedcontinuousdistribution-Funktion</span><span class="sxs-lookup"><span data-stu-id="83e68-102">TransformedContinuousDistribution function</span></span>

<span data-ttu-id="83e68-103">Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="83e68-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="83e68-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="83e68-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="83e68-105">Gibt bei einer kontinuierlichen Verteilung eine neue Verteilung zurück, die den ursprünglichen durch eine angegebene Funktion transformiert.</span><span class="sxs-lookup"><span data-stu-id="83e68-105">Given a continuous distribution, returns a new distribution that transforms the original by a given function.</span></span>

```qsharp
function TransformedContinuousDistribution (transform : (Double -> Double), distribution : Microsoft.Quantum.Random.ContinuousDistribution) : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="input"></a><span data-ttu-id="83e68-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="83e68-106">Input</span></span>

### <a name="transform--double---double"></a><span data-ttu-id="83e68-107">Transformation: [Double](xref:microsoft.quantum.lang-ref.double) -> [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="83e68-107">transform : [Double](xref:microsoft.quantum.lang-ref.double) -> [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="83e68-108">Eine Funktion, die variate der ursprünglichen Verteilung in die transformierte Verteilung umwandelt.</span><span class="sxs-lookup"><span data-stu-id="83e68-108">A function that transforms variates of the original distribution to the transformed distribution.</span></span>


### <a name="distribution--continuousdistribution"></a><span data-ttu-id="83e68-109">Verteilung: [continuousdistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="83e68-109">distribution : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>

<span data-ttu-id="83e68-110">Die ursprüngliche Verteilung, die transformiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="83e68-110">The original distribution to be transformed.</span></span>



## <a name="output--continuousdistribution"></a><span data-ttu-id="83e68-111">Ausgabe: [continuousdistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="83e68-111">Output : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>

<span data-ttu-id="83e68-112">Eine neue Distribution, `distribution` die durch die durch angegebene Transformation verknüpft ist `transform` .</span><span class="sxs-lookup"><span data-stu-id="83e68-112">A new distribution related to `distribution` by the transformation given by `transform`.</span></span>
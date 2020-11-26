---
uid: Microsoft.Quantum.MachineLearning.Sampled
title: Sampling-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: Sampled
qsharp.summary: Samples a given array, using the given schedule.
ms.openlocfilehash: ddff72bbed6f20e8e0ceb3bfe3fc50a3da0bd2a9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211626"
---
# <a name="sampled-function"></a><span data-ttu-id="5da13-102">Sampling-Funktion</span><span class="sxs-lookup"><span data-stu-id="5da13-102">Sampled function</span></span>

<span data-ttu-id="5da13-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="5da13-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="5da13-104">Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="5da13-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="5da13-105">Prüft ein bestimmtes Array unter Verwendung des angegebenen Zeitplans.</span><span class="sxs-lookup"><span data-stu-id="5da13-105">Samples a given array, using the given schedule.</span></span>

```qsharp
function Sampled<'T> (schedule : Microsoft.Quantum.MachineLearning.SamplingSchedule, values : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="5da13-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5da13-106">Input</span></span>

### <a name="schedule--samplingschedule"></a><span data-ttu-id="5da13-107">Zeitplan: [samplingschedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span><span class="sxs-lookup"><span data-stu-id="5da13-107">schedule : [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span></span>

<span data-ttu-id="5da13-108">Ein Zeitplan, der in Stichproben Werten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5da13-108">A schedule to use in sampling values.</span></span>


### <a name="values--t"></a><span data-ttu-id="5da13-109">Werte: 't []</span><span class="sxs-lookup"><span data-stu-id="5da13-109">values : 'T[]</span></span>

<span data-ttu-id="5da13-110">Ein Array von Werten, die abgefragt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5da13-110">An array of values to be sampled.</span></span>



## <a name="output--t"></a><span data-ttu-id="5da13-111">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="5da13-111">Output : 'T[]</span></span>

<span data-ttu-id="5da13-112">Ein Array von-Elementen aus-Werten, das nach dem angegebenen Zeitplan liegt.</span><span class="sxs-lookup"><span data-stu-id="5da13-112">An array of elements from values, following the given schedule.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="5da13-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="5da13-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5da13-114">GIF</span><span class="sxs-lookup"><span data-stu-id="5da13-114">'T</span></span>


---
uid: Microsoft.Quantum.MachineLearning.Sampled
title: Sampling-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: Sampled
qsharp.summary: Samples a given array, using the given schedule.
ms.openlocfilehash: 9f9f91bc50861c5b31a76e28050189d13efda71e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722429"
---
# <a name="sampled-function"></a><span data-ttu-id="9d75b-102">Sampling-Funktion</span><span class="sxs-lookup"><span data-stu-id="9d75b-102">Sampled function</span></span>

<span data-ttu-id="9d75b-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="9d75b-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="9d75b-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9d75b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9d75b-105">Prüft ein bestimmtes Array unter Verwendung des angegebenen Zeitplans.</span><span class="sxs-lookup"><span data-stu-id="9d75b-105">Samples a given array, using the given schedule.</span></span>

```qsharp
function Sampled<'T> (schedule : Microsoft.Quantum.MachineLearning.SamplingSchedule, values : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="9d75b-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9d75b-106">Input</span></span>

### <a name="schedule--samplingschedule"></a><span data-ttu-id="9d75b-107">Zeitplan: [samplingschedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span><span class="sxs-lookup"><span data-stu-id="9d75b-107">schedule : [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span></span>

<span data-ttu-id="9d75b-108">Ein Zeitplan, der in Stichproben Werten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9d75b-108">A schedule to use in sampling values.</span></span>


### <a name="values--t"></a><span data-ttu-id="9d75b-109">Werte: 't []</span><span class="sxs-lookup"><span data-stu-id="9d75b-109">values : 'T[]</span></span>

<span data-ttu-id="9d75b-110">Ein Array von Werten, die abgefragt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9d75b-110">An array of values to be sampled.</span></span>



## <a name="output--t"></a><span data-ttu-id="9d75b-111">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="9d75b-111">Output : 'T[]</span></span>

<span data-ttu-id="9d75b-112">Ein Array von-Elementen aus-Werten, das nach dem angegebenen Zeitplan liegt.</span><span class="sxs-lookup"><span data-stu-id="9d75b-112">An array of elements from values, following the given schedule.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="9d75b-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="9d75b-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="9d75b-114">GIF</span><span class="sxs-lookup"><span data-stu-id="9d75b-114">'T</span></span>


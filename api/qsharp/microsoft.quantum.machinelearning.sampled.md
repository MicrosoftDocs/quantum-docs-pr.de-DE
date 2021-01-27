---
uid: Microsoft.Quantum.MachineLearning.Sampled
title: Sampling-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: Sampled
qsharp.summary: Samples a given array, using the given schedule.
ms.openlocfilehash: 5dd599246847718f4f0411715585cb416595db9d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854950"
---
# <a name="sampled-function"></a><span data-ttu-id="27ed1-102">Sampling-Funktion</span><span class="sxs-lookup"><span data-stu-id="27ed1-102">Sampled function</span></span>

<span data-ttu-id="27ed1-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="27ed1-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="27ed1-104">Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="27ed1-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="27ed1-105">Prüft ein bestimmtes Array unter Verwendung des angegebenen Zeitplans.</span><span class="sxs-lookup"><span data-stu-id="27ed1-105">Samples a given array, using the given schedule.</span></span>

```qsharp
function Sampled<'T> (schedule : Microsoft.Quantum.MachineLearning.SamplingSchedule, values : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="27ed1-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="27ed1-106">Input</span></span>

### <a name="schedule--samplingschedule"></a><span data-ttu-id="27ed1-107">Zeitplan: [samplingschedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span><span class="sxs-lookup"><span data-stu-id="27ed1-107">schedule : [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span></span>

<span data-ttu-id="27ed1-108">Ein Zeitplan, der in Stichproben Werten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="27ed1-108">A schedule to use in sampling values.</span></span>


### <a name="values--t"></a><span data-ttu-id="27ed1-109">Werte: 't []</span><span class="sxs-lookup"><span data-stu-id="27ed1-109">values : 'T[]</span></span>

<span data-ttu-id="27ed1-110">Ein Array von Werten, die abgefragt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="27ed1-110">An array of values to be sampled.</span></span>



## <a name="output--t"></a><span data-ttu-id="27ed1-111">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="27ed1-111">Output : 'T[]</span></span>

<span data-ttu-id="27ed1-112">Ein Array von-Elementen aus-Werten, das nach dem angegebenen Zeitplan liegt.</span><span class="sxs-lookup"><span data-stu-id="27ed1-112">An array of elements from values, following the given schedule.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="27ed1-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="27ed1-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="27ed1-114">GIF</span><span class="sxs-lookup"><span data-stu-id="27ed1-114">'T</span></span>


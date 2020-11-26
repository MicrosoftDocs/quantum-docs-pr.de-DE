---
uid: Microsoft.Quantum.MachineLearning.ScheduleLength
title: Schedulelength-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ScheduleLength
qsharp.summary: Returns the number of elements in a given sampling schedule.
ms.openlocfilehash: 008bdcdc0a7c0ad2775dea65ebba46556092beed
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211592"
---
# <a name="schedulelength-function"></a><span data-ttu-id="2f342-102">Schedulelength-Funktion</span><span class="sxs-lookup"><span data-stu-id="2f342-102">ScheduleLength function</span></span>

<span data-ttu-id="2f342-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="2f342-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="2f342-104">Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="2f342-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="2f342-105">Gibt die Anzahl von Elementen in einem angegebenen Stichproben Zeitplan zurück.</span><span class="sxs-lookup"><span data-stu-id="2f342-105">Returns the number of elements in a given sampling schedule.</span></span>

```qsharp
function ScheduleLength (schedule : Microsoft.Quantum.MachineLearning.SamplingSchedule) : Int
```


## <a name="input"></a><span data-ttu-id="2f342-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2f342-106">Input</span></span>

### <a name="schedule--samplingschedule"></a><span data-ttu-id="2f342-107">Zeitplan: [samplingschedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span><span class="sxs-lookup"><span data-stu-id="2f342-107">schedule : [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span></span>

<span data-ttu-id="2f342-108">Ein Zeitplan für die Stichprobenentnahme, dessen Länge zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="2f342-108">A sampling schedule whose length is to be returned.</span></span>



## <a name="output--int"></a><span data-ttu-id="2f342-109">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2f342-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2f342-110">Die Anzahl der Elemente im angegebenen Stichproben Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="2f342-110">The number of elements in the given sampling schedule.</span></span>
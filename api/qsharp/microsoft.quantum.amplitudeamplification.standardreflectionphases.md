---
uid: Microsoft.Quantum.AmplitudeAmplification.StandardReflectionPhases
title: Standardreflectionphasen-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: StandardReflectionPhases
qsharp.summary: Computes partial reflection phases for standard amplitude amplification.
ms.openlocfilehash: 316c8f22a16859ebb439824eda9a5aa02c750b5d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191124"
---
# <a name="standardreflectionphases-function"></a><span data-ttu-id="eb3a4-102">Standardreflectionphasen-Funktion</span><span class="sxs-lookup"><span data-stu-id="eb3a4-102">StandardReflectionPhases function</span></span>

<span data-ttu-id="eb3a4-103">Namespace: [Microsoft. Quantum. Verstärkungs Verstärkung](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="eb3a4-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="eb3a4-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="eb3a4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="eb3a4-105">Berechnet partielle Reflexionsphasen für die standardmäßige Amplitude-Verstärkung.</span><span class="sxs-lookup"><span data-stu-id="eb3a4-105">Computes partial reflection phases for standard amplitude amplification.</span></span>

```qsharp
function StandardReflectionPhases (nIterations : Int) : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
```


## <a name="input"></a><span data-ttu-id="eb3a4-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="eb3a4-106">Input</span></span>

### <a name="niterations--int"></a><span data-ttu-id="eb3a4-107">niterationen: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="eb3a4-107">nIterations : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="eb3a4-108">Anzahl der Amplitude-Verstärkungs Iterationen, für die partielle Reflexionsphasen generiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="eb3a4-108">Number of amplitude amplification iterations to generate partial reflection phases for.</span></span>



## <a name="output--reflectionphases"></a><span data-ttu-id="eb3a4-109">Ausgabe: [reflectionphasen](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="eb3a4-109">Output : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="eb3a4-110">Ein Vorgang, der als Teil Reflektionen angegebene Phasen implementiert.</span><span class="sxs-lookup"><span data-stu-id="eb3a4-110">An operation that implements phases specified as partial reflections</span></span>

## <a name="remarks"></a><span data-ttu-id="eb3a4-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eb3a4-111">Remarks</span></span>

<span data-ttu-id="eb3a4-112">Alle Phasen sind $ \pi $, mit Ausnahme der ersten Reflektion über den Startstatus und der letzten Reflektion über den Ziel Status ($0 $).</span><span class="sxs-lookup"><span data-stu-id="eb3a4-112">All phases are $\pi$, except for the first reflection about the start state and the last reflection about the target state, which are $0$.</span></span>
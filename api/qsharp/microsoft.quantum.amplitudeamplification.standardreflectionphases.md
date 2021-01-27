---
uid: Microsoft.Quantum.AmplitudeAmplification.StandardReflectionPhases
title: Standardreflectionphasen-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: StandardReflectionPhases
qsharp.summary: Computes partial reflection phases for standard amplitude amplification.
ms.openlocfilehash: 703b50d0186cd0f4eddb9a29fa3cffb2b746c8d6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843914"
---
# <a name="standardreflectionphases-function"></a><span data-ttu-id="5f479-102">Standardreflectionphasen-Funktion</span><span class="sxs-lookup"><span data-stu-id="5f479-102">StandardReflectionPhases function</span></span>

<span data-ttu-id="5f479-103">Namespace: [Microsoft. Quantum. Verstärkungs Verstärkung](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="5f479-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="5f479-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5f479-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5f479-105">Berechnet partielle Reflexionsphasen für die standardmäßige Amplitude-Verstärkung.</span><span class="sxs-lookup"><span data-stu-id="5f479-105">Computes partial reflection phases for standard amplitude amplification.</span></span>

```qsharp
function StandardReflectionPhases (nIterations : Int) : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
```


## <a name="input"></a><span data-ttu-id="5f479-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5f479-106">Input</span></span>

### <a name="niterations--int"></a><span data-ttu-id="5f479-107">niterationen: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5f479-107">nIterations : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5f479-108">Anzahl der Amplitude-Verstärkungs Iterationen, für die partielle Reflexionsphasen generiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5f479-108">Number of amplitude amplification iterations to generate partial reflection phases for.</span></span>



## <a name="output--reflectionphases"></a><span data-ttu-id="5f479-109">Ausgabe: [reflectionphasen](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="5f479-109">Output : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="5f479-110">Ein Vorgang, der als Teil Reflektionen angegebene Phasen implementiert.</span><span class="sxs-lookup"><span data-stu-id="5f479-110">An operation that implements phases specified as partial reflections</span></span>

## <a name="remarks"></a><span data-ttu-id="5f479-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5f479-111">Remarks</span></span>

<span data-ttu-id="5f479-112">Alle Phasen sind $ \pi $, mit Ausnahme der ersten Reflektion über den Startstatus und der letzten Reflektion über den Ziel Status ($0 $).</span><span class="sxs-lookup"><span data-stu-id="5f479-112">All phases are $\pi$, except for the first reflection about the start state and the last reflection about the target state, which are $0$.</span></span>
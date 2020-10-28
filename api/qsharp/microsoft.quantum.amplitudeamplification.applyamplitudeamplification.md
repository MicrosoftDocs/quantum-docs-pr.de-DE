---
uid: Microsoft.Quantum.AmplitudeAmplification.ApplyAmplitudeAmplification
title: Applyverstärktudeverstärkungsvorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ApplyAmplitudeAmplification
qsharp.summary: Applies amplitude amplification on a given register, using a given set of phases and oracles to reflect about the initial and final states.
ms.openlocfilehash: be884eab70c7f72f994baf6bd7caf05769e0d5f2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92721926"
---
# <a name="applyamplitudeamplification-operation"></a><span data-ttu-id="d0a01-102">Applyverstärktudeverstärkungsvorgang</span><span class="sxs-lookup"><span data-stu-id="d0a01-102">ApplyAmplitudeAmplification operation</span></span>

<span data-ttu-id="d0a01-103">Namespace: [Microsoft. Quantum. Verstärkungs Verstärkung](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="d0a01-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="d0a01-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d0a01-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d0a01-105">Wendet die Amplitude-Verstärkung für ein angegebenes Register an, wobei eine bestimmte Reihe von Phasen und Oracles verwendet werden, um den ursprünglichen und den Endzustand widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="d0a01-105">Applies amplitude amplification on a given register, using a given set of phases and oracles to reflect about the initial and final states.</span></span>

```qsharp
operation ApplyAmplitudeAmplification (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, startStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, targetStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="d0a01-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d0a01-106">Input</span></span>

### <a name="phases--reflectionphases"></a><span data-ttu-id="d0a01-107">Phasen: [reflectionphasen](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="d0a01-107">phases : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="d0a01-108">Ein Satz von Phasen, in denen die partiellen Reflektionen bei jedem Schritt des Amplitude-Verstärkungs Algorithmus beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="d0a01-108">A set of phases describing the partial reflections at each step of the amplitude amplification algorithm.</span></span> <span data-ttu-id="d0a01-109">Ein Beispiel finden Sie unter @"microsoft.quantum.amplitudeamplification.standardreflectionphases".</span><span class="sxs-lookup"><span data-stu-id="d0a01-109">See @"microsoft.quantum.amplitudeamplification.standardreflectionphases" for an example.</span></span>


### <a name="startstatereflection--reflectionoracle"></a><span data-ttu-id="d0a01-110">Startstatus-eflection: [reflectionoracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="d0a01-110">startStateReflection : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="d0a01-111">Ein Oracle, das den ursprünglichen Zustand reflektiert.</span><span class="sxs-lookup"><span data-stu-id="d0a01-111">An oracle that reflects about the initial state.</span></span>


### <a name="targetstatereflection--reflectionoracle"></a><span data-ttu-id="d0a01-112">targetstatuereflection: [reflectionoracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="d0a01-112">targetStateReflection : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="d0a01-113">Ein Oracle, das den gewünschten Endzustand reflektiert.</span><span class="sxs-lookup"><span data-stu-id="d0a01-113">An oracle that reflects about the desired final state.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="d0a01-114">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="d0a01-114">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="d0a01-115">Ein Register zum Durchführen der Amplitude-Verstärkung.</span><span class="sxs-lookup"><span data-stu-id="d0a01-115">A register to perform amplitude amplification on.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d0a01-116">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d0a01-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>


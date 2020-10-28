---
uid: Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
title: Reflectionphasen-benutzerdefinierter Typ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ReflectionPhases
qsharp.summary: Phases for a sequence of partial reflections in amplitude amplification.
ms.openlocfilehash: e0c7db6cd1aad636a34684958be117de1b9888f8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92721814"
---
# <a name="reflectionphases-user-defined-type"></a><span data-ttu-id="80b95-102">Reflectionphasen-benutzerdefinierter Typ</span><span class="sxs-lookup"><span data-stu-id="80b95-102">ReflectionPhases user defined type</span></span>

<span data-ttu-id="80b95-103">Namespace: [Microsoft. Quantum. Verstärkungs Verstärkung](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="80b95-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="80b95-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="80b95-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="80b95-105">Phasen für eine Sequenz von partiellen Reflektionen bei der Amplitude-Verstärkung.</span><span class="sxs-lookup"><span data-stu-id="80b95-105">Phases for a sequence of partial reflections in amplitude amplification.</span></span>

```qsharp

newtype ReflectionPhases = (AboutStart : Double[], AboutTarget : Double[]);
```



## <a name="named-items"></a><span data-ttu-id="80b95-106">Benannte Elemente</span><span class="sxs-lookup"><span data-stu-id="80b95-106">Named Items</span></span>

### <a name="aboutstart--double"></a><span data-ttu-id="80b95-107">Aboutstart: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="80b95-107">AboutStart : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="80b95-108">Ein Array von Phasen für die Reflektion über den Startzustand.</span><span class="sxs-lookup"><span data-stu-id="80b95-108">An array of phases for reflection about the start state.</span></span>
### <a name="abouttarget--double"></a><span data-ttu-id="80b95-109">Abouttarget: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="80b95-109">AboutTarget : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="80b95-110">Ein Array von Phasen für die Reflektion über den Zielzustand.</span><span class="sxs-lookup"><span data-stu-id="80b95-110">An array of phases for reflection about the target state.</span></span>

## <a name="remarks"></a><span data-ttu-id="80b95-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="80b95-111">Remarks</span></span>

<span data-ttu-id="80b95-112">Beide Arrays müssen die gleiche Länge aufweisen.</span><span class="sxs-lookup"><span data-stu-id="80b95-112">Both arrays must be of equal length.</span></span> <span data-ttu-id="80b95-113">Beachten Sie, dass in vielen Fällen in der ersten Phase für den Startstatus und die letzte Phase zum Ziel Status eine globale Phasenverschiebung eingeführt und möglicherweise auf $0 $ festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="80b95-113">Note that in many cases, the first phase about the start state and last phase about the target state introduces a global phase shift and may be set to $0$.</span></span>
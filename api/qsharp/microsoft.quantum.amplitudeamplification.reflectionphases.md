---
uid: Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
title: Reflectionphasen-benutzerdefinierter Typ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ReflectionPhases
qsharp.summary: Phases for a sequence of partial reflections in amplitude amplification.
ms.openlocfilehash: fc3642b76c6e01f0709e78ea42c9ea7237389afa
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847179"
---
# <a name="reflectionphases-user-defined-type"></a><span data-ttu-id="4a83c-102">Reflectionphasen-benutzerdefinierter Typ</span><span class="sxs-lookup"><span data-stu-id="4a83c-102">ReflectionPhases user defined type</span></span>

<span data-ttu-id="4a83c-103">Namespace: [Microsoft. Quantum. Verstärkungs Verstärkung](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="4a83c-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="4a83c-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4a83c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4a83c-105">Phasen für eine Sequenz von partiellen Reflektionen bei der Amplitude-Verstärkung.</span><span class="sxs-lookup"><span data-stu-id="4a83c-105">Phases for a sequence of partial reflections in amplitude amplification.</span></span>

```qsharp

newtype ReflectionPhases = (AboutStart : Double[], AboutTarget : Double[]);
```



## <a name="named-items"></a><span data-ttu-id="4a83c-106">Benannte Elemente</span><span class="sxs-lookup"><span data-stu-id="4a83c-106">Named Items</span></span>

### <a name="aboutstart--double"></a><span data-ttu-id="4a83c-107">Aboutstart: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="4a83c-107">AboutStart : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="4a83c-108">Ein Array von Phasen für die Reflektion über den Startzustand.</span><span class="sxs-lookup"><span data-stu-id="4a83c-108">An array of phases for reflection about the start state.</span></span>
### <a name="abouttarget--double"></a><span data-ttu-id="4a83c-109">Abouttarget: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="4a83c-109">AboutTarget : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="4a83c-110">Ein Array von Phasen für die Reflektion über den Zielzustand.</span><span class="sxs-lookup"><span data-stu-id="4a83c-110">An array of phases for reflection about the target state.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a83c-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a83c-111">Remarks</span></span>

<span data-ttu-id="4a83c-112">Beide Arrays müssen die gleiche Länge aufweisen.</span><span class="sxs-lookup"><span data-stu-id="4a83c-112">Both arrays must be of equal length.</span></span> <span data-ttu-id="4a83c-113">Beachten Sie, dass in vielen Fällen in der ersten Phase für den Startstatus und die letzte Phase zum Ziel Status eine globale Phasenverschiebung eingeführt und möglicherweise auf $0 $ festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="4a83c-113">Note that in many cases, the first phase about the start state and last phase about the target state introduces a global phase shift and may be set to $0$.</span></span>
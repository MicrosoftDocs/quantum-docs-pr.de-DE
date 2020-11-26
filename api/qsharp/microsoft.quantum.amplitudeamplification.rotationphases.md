---
uid: Microsoft.Quantum.AmplitudeAmplification.RotationPhases
title: Benutzerdefinierter Typ "rotationphasen"
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: RotationPhases
qsharp.summary: Phases for a sequence of single-qubit rotations in amplitude amplification.
ms.openlocfilehash: 60fcda7d58a19f8891e252ddb18b504afddf5514
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191362"
---
# <a name="rotationphases-user-defined-type"></a><span data-ttu-id="df2dd-102">Benutzerdefinierter Typ "rotationphasen"</span><span class="sxs-lookup"><span data-stu-id="df2dd-102">RotationPhases user defined type</span></span>

<span data-ttu-id="df2dd-103">Namespace: [Microsoft. Quantum. Verstärkungs Verstärkung](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="df2dd-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="df2dd-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="df2dd-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="df2dd-105">Phasen für eine Sequenz von Single-Qubit-Drehungen in der Amplitude-Verstärkung.</span><span class="sxs-lookup"><span data-stu-id="df2dd-105">Phases for a sequence of single-qubit rotations in amplitude amplification.</span></span>

```qsharp

newtype RotationPhases = (Double[]);
```



## <a name="remarks"></a><span data-ttu-id="df2dd-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="df2dd-106">Remarks</span></span>

<span data-ttu-id="df2dd-107">Der erste Parameter ist ein Array von Phasen für Reflektionen, ausgedrückt als Produkt von Single-Qubit-Drehungen.</span><span class="sxs-lookup"><span data-stu-id="df2dd-107">The first parameter is an array of phases for reflections, expressed as a product of single-qubit rotations.</span></span>
<span data-ttu-id="df2dd-108">[G.H.</span><span class="sxs-lookup"><span data-stu-id="df2dd-108">[ G.H.</span></span> <span data-ttu-id="df2dd-109">Niedrig, I. L.</span><span class="sxs-lookup"><span data-stu-id="df2dd-109">Low, I. L.</span></span> <span data-ttu-id="df2dd-110">Chuang, https://arxiv.org/abs/1707.05391 ].</span><span class="sxs-lookup"><span data-stu-id="df2dd-110">Chuang, https://arxiv.org/abs/1707.05391].</span></span>
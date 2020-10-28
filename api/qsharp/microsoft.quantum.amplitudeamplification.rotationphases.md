---
uid: Microsoft.Quantum.AmplitudeAmplification.RotationPhases
title: Benutzerdefinierter Typ "rotationphasen"
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: RotationPhases
qsharp.summary: Phases for a sequence of single-qubit rotations in amplitude amplification.
ms.openlocfilehash: b0373f964b77f8ea561c6e96b11e476b42e7fc55
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92721771"
---
# <a name="rotationphases-user-defined-type"></a><span data-ttu-id="03cc5-102">Benutzerdefinierter Typ "rotationphasen"</span><span class="sxs-lookup"><span data-stu-id="03cc5-102">RotationPhases user defined type</span></span>

<span data-ttu-id="03cc5-103">Namespace: [Microsoft. Quantum. Verstärkungs Verstärkung](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="03cc5-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="03cc5-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="03cc5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="03cc5-105">Phasen für eine Sequenz von Single-Qubit-Drehungen in der Amplitude-Verstärkung.</span><span class="sxs-lookup"><span data-stu-id="03cc5-105">Phases for a sequence of single-qubit rotations in amplitude amplification.</span></span>

```qsharp

newtype RotationPhases = (Double[]);
```



## <a name="remarks"></a><span data-ttu-id="03cc5-106">Hinweise</span><span class="sxs-lookup"><span data-stu-id="03cc5-106">Remarks</span></span>

<span data-ttu-id="03cc5-107">Der erste Parameter ist ein Array von Phasen für Reflektionen, ausgedrückt als Produkt von Single-Qubit-Drehungen.</span><span class="sxs-lookup"><span data-stu-id="03cc5-107">The first parameter is an array of phases for reflections, expressed as a product of single-qubit rotations.</span></span>
<span data-ttu-id="03cc5-108">[G.H.</span><span class="sxs-lookup"><span data-stu-id="03cc5-108">[ G.H.</span></span> <span data-ttu-id="03cc5-109">Niedrig, I. L.</span><span class="sxs-lookup"><span data-stu-id="03cc5-109">Low, I. L.</span></span> <span data-ttu-id="03cc5-110">Chuang, https://arxiv.org/abs/1707.05391 ].</span><span class="sxs-lookup"><span data-stu-id="03cc5-110">Chuang, https://arxiv.org/abs/1707.05391].</span></span>
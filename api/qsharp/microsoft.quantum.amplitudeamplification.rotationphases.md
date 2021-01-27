---
uid: Microsoft.Quantum.AmplitudeAmplification.RotationPhases
title: Benutzerdefinierter Typ "rotationphasen"
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: RotationPhases
qsharp.summary: Phases for a sequence of single-qubit rotations in amplitude amplification.
ms.openlocfilehash: 2f955ce3bfb9ea057c26c79547895df39ed322ab
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843962"
---
# <a name="rotationphases-user-defined-type"></a><span data-ttu-id="a6aa8-102">Benutzerdefinierter Typ "rotationphasen"</span><span class="sxs-lookup"><span data-stu-id="a6aa8-102">RotationPhases user defined type</span></span>

<span data-ttu-id="a6aa8-103">Namespace: [Microsoft. Quantum. Verstärkungs Verstärkung](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="a6aa8-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="a6aa8-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a6aa8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a6aa8-105">Phasen für eine Sequenz von Single-Qubit-Drehungen in der Amplitude-Verstärkung.</span><span class="sxs-lookup"><span data-stu-id="a6aa8-105">Phases for a sequence of single-qubit rotations in amplitude amplification.</span></span>

```qsharp

newtype RotationPhases = (Double[]);
```



## <a name="remarks"></a><span data-ttu-id="a6aa8-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a6aa8-106">Remarks</span></span>

<span data-ttu-id="a6aa8-107">Der erste Parameter ist ein Array von Phasen für Reflektionen, ausgedrückt als Produkt von Single-Qubit-Drehungen.</span><span class="sxs-lookup"><span data-stu-id="a6aa8-107">The first parameter is an array of phases for reflections, expressed as a product of single-qubit rotations.</span></span>
<span data-ttu-id="a6aa8-108">[G.H.</span><span class="sxs-lookup"><span data-stu-id="a6aa8-108">[ G.H.</span></span> <span data-ttu-id="a6aa8-109">Niedrig, I. L.</span><span class="sxs-lookup"><span data-stu-id="a6aa8-109">Low, I. L.</span></span> <span data-ttu-id="a6aa8-110">Chuang, https://arxiv.org/abs/1707.05391 ].</span><span class="sxs-lookup"><span data-stu-id="a6aa8-110">Chuang, https://arxiv.org/abs/1707.05391].</span></span>
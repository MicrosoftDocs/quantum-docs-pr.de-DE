---
uid: Microsoft.Quantum.AmplitudeAmplification.RotationPhasesAsReflectionPhases
title: Rotationphasesasreflectionphasen-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: RotationPhasesAsReflectionPhases
qsharp.summary: Converts phases specified as single-qubit rotations to phases specified as partial reflections.
ms.openlocfilehash: 5d50b3fdc2b0f948e93cb11b5c69403d97574ccd
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843957"
---
# <a name="rotationphasesasreflectionphases-function"></a><span data-ttu-id="77dc6-102">Rotationphasesasreflectionphasen-Funktion</span><span class="sxs-lookup"><span data-stu-id="77dc6-102">RotationPhasesAsReflectionPhases function</span></span>

<span data-ttu-id="77dc6-103">Namespace: [Microsoft. Quantum. Verstärkungs Verstärkung](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="77dc6-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="77dc6-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="77dc6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="77dc6-105">Konvertiert als Single-Qubit-Drehungen angegebene Phasen in Phasen, die als partielle Reflektionen angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="77dc6-105">Converts phases specified as single-qubit rotations to phases specified as partial reflections.</span></span>

```qsharp
function RotationPhasesAsReflectionPhases (rotPhases : Microsoft.Quantum.AmplitudeAmplification.RotationPhases) : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
```


## <a name="input"></a><span data-ttu-id="77dc6-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="77dc6-106">Input</span></span>

### <a name="rotphases--rotationphases"></a><span data-ttu-id="77dc6-107">rotphasen: [rotationphasen](xref:Microsoft.Quantum.AmplitudeAmplification.RotationPhases)</span><span class="sxs-lookup"><span data-stu-id="77dc6-107">rotPhases : [RotationPhases](xref:Microsoft.Quantum.AmplitudeAmplification.RotationPhases)</span></span>

<span data-ttu-id="77dc6-108">Array von Single-Qubit-Drehungen, das in partielle Reflektionen konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="77dc6-108">Array of single-qubit rotations to be converted to partial reflections.</span></span>



## <a name="output--reflectionphases"></a><span data-ttu-id="77dc6-109">Ausgabe: [reflectionphasen](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="77dc6-109">Output : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="77dc6-110">Ein Vorgang, der Phasen implementiert, die als Teil Spiegelungen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="77dc6-110">An operation that implements phases specified as partial reflections.</span></span>

## <a name="references"></a><span data-ttu-id="77dc6-111">References</span><span class="sxs-lookup"><span data-stu-id="77dc6-111">References</span></span>

<span data-ttu-id="77dc6-112">Wir verwenden die Konvention in</span><span class="sxs-lookup"><span data-stu-id="77dc6-112">We use the convention in</span></span>

- <span data-ttu-id="77dc6-113">[ *G.H. Low, I. L. Chuang*](https://arxiv.org/abs/1707.05391) zum Verknüpfen von Single-Qubit-Rotations Phasen mit reflektionsoperator-Phasen.</span><span class="sxs-lookup"><span data-stu-id="77dc6-113">[ *G.H. Low, I. L. Chuang* ](https://arxiv.org/abs/1707.05391) for relating single-qubit rotation phases to reflection operator phases.</span></span>
---
uid: Microsoft.Quantum.Preparation.MixedStatePreparation
title: Mixedstatepreparation-benutzerdefinierter Typ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: MixedStatePreparation
qsharp.summary: Represents a particular mixed state that can be prepared on an index and a garbage register.
ms.openlocfilehash: 7e5b6ca755aac19a31b7e27e32e934bb823b128e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842407"
---
# <a name="mixedstatepreparation-user-defined-type"></a><span data-ttu-id="7e0fe-102">Mixedstatepreparation-benutzerdefinierter Typ</span><span class="sxs-lookup"><span data-stu-id="7e0fe-102">MixedStatePreparation user defined type</span></span>

<span data-ttu-id="7e0fe-103">Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="7e0fe-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="7e0fe-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7e0fe-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7e0fe-105">Stellt einen bestimmten gemischten Zustand dar, der für einen Index und ein Garbage Register vorbereitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7e0fe-105">Represents a particular mixed state that can be prepared on an index and a garbage register.</span></span>

```qsharp

newtype MixedStatePreparation = (Requirements : Microsoft.Quantum.Preparation.MixedStatePreparationRequirements, Norm : Double, Prepare : ((Microsoft.Quantum.Arithmetic.LittleEndian, Qubit[], Qubit[]) => Unit is Adj + Ctl));
```



## <a name="named-items"></a><span data-ttu-id="7e0fe-106">Benannte Elemente</span><span class="sxs-lookup"><span data-stu-id="7e0fe-106">Named Items</span></span>

### <a name="requirements--mixedstatepreparationrequirements"></a><span data-ttu-id="7e0fe-107">Anforderungen: [mixedstatepreparationrequirements](xref:Microsoft.Quantum.Preparation.MixedStatePreparationRequirements)</span><span class="sxs-lookup"><span data-stu-id="7e0fe-107">Requirements : [MixedStatePreparationRequirements](xref:Microsoft.Quantum.Preparation.MixedStatePreparationRequirements)</span></span>


### <a name="norm--double"></a><span data-ttu-id="7e0fe-108">Norm: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="7e0fe-108">Norm : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>


### <a name="prepare--littleendianqubitqubit--unit--is-adj--ctl"></a><span data-ttu-id="7e0fe-109">Prepare: ([littleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="7e0fe-109">Prepare : ([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>



## <a name="see-also"></a><span data-ttu-id="7e0fe-110">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7e0fe-110">See Also</span></span>

- [<span data-ttu-id="7e0fe-111">Microsoft. Quantum. purifedmixedstate</span><span class="sxs-lookup"><span data-stu-id="7e0fe-111">Microsoft.Quantum.PurifiedMixedState</span></span>](xref:Microsoft.Quantum.PurifiedMixedState)
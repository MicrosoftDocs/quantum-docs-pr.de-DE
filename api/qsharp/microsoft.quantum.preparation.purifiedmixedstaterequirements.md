---
uid: Microsoft.Quantum.Preparation.PurifiedMixedStateRequirements
title: Purifedmixedstatuerequirequirements-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PurifiedMixedStateRequirements
qsharp.summary: Returns the total number of qubits that must be allocated in order to apply the operation returned by @"microsoft.quantum.preparation.purifiedmixedstate".
ms.openlocfilehash: 9b8861a4112c4e6c9db994339353c771a3de81a6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229986"
---
# <a name="purifiedmixedstaterequirements-function"></a><span data-ttu-id="d2d77-102">Purifedmixedstatuerequirequirements-Funktion</span><span class="sxs-lookup"><span data-stu-id="d2d77-102">PurifiedMixedStateRequirements function</span></span>

<span data-ttu-id="d2d77-103">Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="d2d77-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="d2d77-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d2d77-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d2d77-105">Gibt die Gesamtzahl der Qubits zurück, die zugeordnet werden müssen, um den von zurückgegebenen Vorgang anzuwenden @"microsoft.quantum.preparation.purifiedmixedstate" .</span><span class="sxs-lookup"><span data-stu-id="d2d77-105">Returns the total number of qubits that must be allocated in order to apply the operation returned by @"microsoft.quantum.preparation.purifiedmixedstate".</span></span>

```qsharp
function PurifiedMixedStateRequirements (targetError : Double, nCoefficients : Int) : Microsoft.Quantum.Preparation.MixedStatePreparationRequirements
```


## <a name="input"></a><span data-ttu-id="d2d77-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d2d77-106">Input</span></span>

### <a name="targeterror--double"></a><span data-ttu-id="d2d77-107">targeterror: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="d2d77-107">targetError : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="d2d77-108">Der Ziel Fehler $ \epsilon $.</span><span class="sxs-lookup"><span data-stu-id="d2d77-108">The target error $\epsilon$.</span></span>


### <a name="ncoefficients--int"></a><span data-ttu-id="d2d77-109">nkoeffizienten: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d2d77-109">nCoefficients : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d2d77-110">Die Anzahl der Koeffizienten, die beim Vorbereiten eines gemischten Zustands angegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d2d77-110">The number of coefficients to be specified in preparing a mixed state.</span></span>



## <a name="output--mixedstatepreparationrequirements"></a><span data-ttu-id="d2d77-111">Ausgabe: [mixedstatepreparationrequirements](xref:Microsoft.Quantum.Preparation.MixedStatePreparationRequirements)</span><span class="sxs-lookup"><span data-stu-id="d2d77-111">Output : [MixedStatePreparationRequirements](xref:Microsoft.Quantum.Preparation.MixedStatePreparationRequirements)</span></span>

<span data-ttu-id="d2d77-112">Eine Beschreibung, wie viele Qubits insgesamt erforderlich sind, und für jeden Index und die von der Funktion verwendeten Garbage Registern @"microsoft.quantum.preparation.purifiedmixedstate" .</span><span class="sxs-lookup"><span data-stu-id="d2d77-112">A description of how many qubits are required in total, and for each of the index and garbage registers used by the @"microsoft.quantum.preparation.purifiedmixedstate" function.</span></span>

## <a name="see-also"></a><span data-ttu-id="d2d77-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d2d77-113">See Also</span></span>

- [<span data-ttu-id="d2d77-114">Microsoft. Quantum. Preparation. purifedmixedstate</span><span class="sxs-lookup"><span data-stu-id="d2d77-114">Microsoft.Quantum.Preparation.PurifiedMixedState</span></span>](xref:Microsoft.Quantum.Preparation.PurifiedMixedState)
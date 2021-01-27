---
uid: Microsoft.Quantum.Preparation.PurifiedMixedStateRequirements
title: Purifedmixedstatuerequirequirements-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PurifiedMixedStateRequirements
qsharp.summary: Returns the total number of qubits that must be allocated in order to apply the operation returned by @"microsoft.quantum.preparation.purifiedmixedstate".
ms.openlocfilehash: 6ddb48ba66eea87a07d515ff791bfb34f2d98b76
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856829"
---
# <a name="purifiedmixedstaterequirements-function"></a><span data-ttu-id="1e959-102">Purifedmixedstatuerequirequirements-Funktion</span><span class="sxs-lookup"><span data-stu-id="1e959-102">PurifiedMixedStateRequirements function</span></span>

<span data-ttu-id="1e959-103">Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="1e959-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="1e959-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1e959-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1e959-105">Gibt die Gesamtzahl der Qubits zurück, die zugeordnet werden müssen, um den von zurückgegebenen Vorgang anzuwenden @"microsoft.quantum.preparation.purifiedmixedstate" .</span><span class="sxs-lookup"><span data-stu-id="1e959-105">Returns the total number of qubits that must be allocated in order to apply the operation returned by @"microsoft.quantum.preparation.purifiedmixedstate".</span></span>

```qsharp
function PurifiedMixedStateRequirements (targetError : Double, nCoefficients : Int) : Microsoft.Quantum.Preparation.MixedStatePreparationRequirements
```


## <a name="input"></a><span data-ttu-id="1e959-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1e959-106">Input</span></span>

### <a name="targeterror--double"></a><span data-ttu-id="1e959-107">targeterror: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="1e959-107">targetError : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="1e959-108">Der Ziel Fehler $ \epsilon $.</span><span class="sxs-lookup"><span data-stu-id="1e959-108">The target error $\epsilon$.</span></span>


### <a name="ncoefficients--int"></a><span data-ttu-id="1e959-109">nkoeffizienten: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="1e959-109">nCoefficients : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="1e959-110">Die Anzahl der Koeffizienten, die beim Vorbereiten eines gemischten Zustands angegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1e959-110">The number of coefficients to be specified in preparing a mixed state.</span></span>



## <a name="output--mixedstatepreparationrequirements"></a><span data-ttu-id="1e959-111">Ausgabe: [mixedstatepreparationrequirements](xref:Microsoft.Quantum.Preparation.MixedStatePreparationRequirements)</span><span class="sxs-lookup"><span data-stu-id="1e959-111">Output : [MixedStatePreparationRequirements](xref:Microsoft.Quantum.Preparation.MixedStatePreparationRequirements)</span></span>

<span data-ttu-id="1e959-112">Eine Beschreibung, wie viele Qubits insgesamt erforderlich sind, und für jeden Index und die von der Funktion verwendeten Garbage Registern @"microsoft.quantum.preparation.purifiedmixedstate" .</span><span class="sxs-lookup"><span data-stu-id="1e959-112">A description of how many qubits are required in total, and for each of the index and garbage registers used by the @"microsoft.quantum.preparation.purifiedmixedstate" function.</span></span>

## <a name="see-also"></a><span data-ttu-id="1e959-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1e959-113">See Also</span></span>

- [<span data-ttu-id="1e959-114">Microsoft. Quantum. Preparation. purifedmixedstate</span><span class="sxs-lookup"><span data-stu-id="1e959-114">Microsoft.Quantum.Preparation.PurifiedMixedState</span></span>](xref:Microsoft.Quantum.Preparation.PurifiedMixedState)
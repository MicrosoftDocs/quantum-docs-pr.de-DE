---
uid: Microsoft.Quantum.ErrorCorrection.FiveQubitCode
title: "\"Fvequbitcode\"-Funktion"
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: FiveQubitCode
qsharp.summary: Returns a QECC value representing the ⟦5, 1, 3⟧ code encoder and decoder with in-place syndrome measurement.
ms.openlocfilehash: 7509de880b1e3ea8964b61e4b3f034ce20b2f202
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702485"
---
# <a name="fivequbitcode-function"></a><span data-ttu-id="219a4-102">"Fvequbitcode"-Funktion</span><span class="sxs-lookup"><span data-stu-id="219a4-102">FiveQubitCode function</span></span>

<span data-ttu-id="219a4-103">Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="219a4-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="219a4-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="219a4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="219a4-105">Gibt einen qecc-Wert zurück, der den ⟦ 5, 1, 3 ⟧ Code Encoder und den Decoder mit der direkten Messung darstellt.</span><span class="sxs-lookup"><span data-stu-id="219a4-105">Returns a QECC value representing the ⟦5, 1, 3⟧ code encoder and decoder with in-place syndrome measurement.</span></span>

```qsharp
function FiveQubitCode () : Microsoft.Quantum.ErrorCorrection.QECC
```


## <a name="output--qecc"></a><span data-ttu-id="219a4-106">Ausgabe: [qecc](xref:Microsoft.Quantum.ErrorCorrection.QECC)</span><span class="sxs-lookup"><span data-stu-id="219a4-106">Output : [QECC](xref:Microsoft.Quantum.ErrorCorrection.QECC)</span></span>

<span data-ttu-id="219a4-107">Gibt eine Implementierung eines Quantum-Fehlerkorrekturcodes zurück, indem ein-Typ angegeben wird `QECC` .</span><span class="sxs-lookup"><span data-stu-id="219a4-107">Returns an implementation of a quantum error correction code by specifying a `QECC` type.</span></span>

## <a name="remarks"></a><span data-ttu-id="219a4-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="219a4-108">Remarks</span></span>

<span data-ttu-id="219a4-109">Dieser Code wurde in den folgenden zwei Dokumenten unabhängig voneinander gefunden:</span><span class="sxs-lookup"><span data-stu-id="219a4-109">This code was found independently in the following two papers:</span></span>

- <span data-ttu-id="219a4-110">C.</span><span class="sxs-lookup"><span data-stu-id="219a4-110">C.</span></span> <span data-ttu-id="219a4-111">H.</span><span class="sxs-lookup"><span data-stu-id="219a4-111">H.</span></span> <span data-ttu-id="219a4-112">Bennett, D. divincenzo, J. A.</span><span class="sxs-lookup"><span data-stu-id="219a4-112">Bennett, D. DiVincenzo, J. A.</span></span> <span data-ttu-id="219a4-113">Smolin und W. K.</span><span class="sxs-lookup"><span data-stu-id="219a4-113">Smolin and W. K.</span></span> <span data-ttu-id="219a4-114">Wootters, "gemischte Zustands jede Verflechtungen und Quantum-Fehlerkorrektur", "Phys. Rev. A, 54 (1996) PP. 3824-3851; https://arxiv.org/abs/quant-ph/9604024 und</span><span class="sxs-lookup"><span data-stu-id="219a4-114">Wootters, "Mixed state entanglement and quantum error correction," Phys. Rev. A, 54 (1996) pp. 3824-3851; https://arxiv.org/abs/quant-ph/9604024 and</span></span>
- <span data-ttu-id="219a4-115">R.</span><span class="sxs-lookup"><span data-stu-id="219a4-115">R.</span></span> <span data-ttu-id="219a4-116">Laflamme, C. Miquel, J. P.</span><span class="sxs-lookup"><span data-stu-id="219a4-116">Laflamme, C. Miquel, J. P.</span></span> <span data-ttu-id="219a4-117">Paz und W. H.</span><span class="sxs-lookup"><span data-stu-id="219a4-117">Paz and W. H.</span></span> <span data-ttu-id="219a4-118">Zurek, "Perfect Quantum Error Korrektur Code", "Phys. Rev. Lett.</span><span class="sxs-lookup"><span data-stu-id="219a4-118">Zurek, "Perfect quantum error correction code," Phys. Rev. Lett.</span></span> <span data-ttu-id="219a4-119">77 (1996) PP. 198-201; https://arxiv.org/abs/quant-ph/9602019</span><span class="sxs-lookup"><span data-stu-id="219a4-119">77 (1996) pp. 198-201; https://arxiv.org/abs/quant-ph/9602019</span></span>
---
uid: Microsoft.Quantum.ErrorCorrection.FiveQubitCode
title: "\"Fvequbitcode\"-Funktion"
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: FiveQubitCode
qsharp.summary: Returns a QECC value representing the ⟦5, 1, 3⟧ code encoder and decoder with in-place syndrome measurement.
ms.openlocfilehash: 3b45af29897735905f7fe52340e2a8e425bd8cbe
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200882"
---
# <a name="fivequbitcode-function"></a><span data-ttu-id="c2f7d-102">"Fvequbitcode"-Funktion</span><span class="sxs-lookup"><span data-stu-id="c2f7d-102">FiveQubitCode function</span></span>

<span data-ttu-id="c2f7d-103">Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="c2f7d-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="c2f7d-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c2f7d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c2f7d-105">Gibt einen qecc-Wert zurück, der den ⟦ 5, 1, 3 ⟧ Code Encoder und den Decoder mit der direkten Messung darstellt.</span><span class="sxs-lookup"><span data-stu-id="c2f7d-105">Returns a QECC value representing the ⟦5, 1, 3⟧ code encoder and decoder with in-place syndrome measurement.</span></span>

```qsharp
function FiveQubitCode () : Microsoft.Quantum.ErrorCorrection.QECC
```


## <a name="output--qecc"></a><span data-ttu-id="c2f7d-106">Ausgabe: [qecc](xref:Microsoft.Quantum.ErrorCorrection.QECC)</span><span class="sxs-lookup"><span data-stu-id="c2f7d-106">Output : [QECC](xref:Microsoft.Quantum.ErrorCorrection.QECC)</span></span>

<span data-ttu-id="c2f7d-107">Gibt eine Implementierung eines Quantum-Fehlerkorrekturcodes zurück, indem ein-Typ angegeben wird `QECC` .</span><span class="sxs-lookup"><span data-stu-id="c2f7d-107">Returns an implementation of a quantum error correction code by specifying a `QECC` type.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2f7d-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c2f7d-108">Remarks</span></span>

<span data-ttu-id="c2f7d-109">Dieser Code wurde in den folgenden zwei Dokumenten unabhängig voneinander gefunden:</span><span class="sxs-lookup"><span data-stu-id="c2f7d-109">This code was found independently in the following two papers:</span></span>

- <span data-ttu-id="c2f7d-110">C.</span><span class="sxs-lookup"><span data-stu-id="c2f7d-110">C.</span></span> <span data-ttu-id="c2f7d-111">H.</span><span class="sxs-lookup"><span data-stu-id="c2f7d-111">H.</span></span> <span data-ttu-id="c2f7d-112">Bennett, D. divincenzo, J. A.</span><span class="sxs-lookup"><span data-stu-id="c2f7d-112">Bennett, D. DiVincenzo, J. A.</span></span> <span data-ttu-id="c2f7d-113">Smolin und W. K.</span><span class="sxs-lookup"><span data-stu-id="c2f7d-113">Smolin and W. K.</span></span> <span data-ttu-id="c2f7d-114">Wootters, "gemischte Zustands jede Verflechtungen und Quantum-Fehlerkorrektur", "Phys. Rev. A, 54 (1996) PP. 3824-3851; https://arxiv.org/abs/quant-ph/9604024 und</span><span class="sxs-lookup"><span data-stu-id="c2f7d-114">Wootters, "Mixed state entanglement and quantum error correction," Phys. Rev. A, 54 (1996) pp. 3824-3851; https://arxiv.org/abs/quant-ph/9604024 and</span></span>
- <span data-ttu-id="c2f7d-115">R.</span><span class="sxs-lookup"><span data-stu-id="c2f7d-115">R.</span></span> <span data-ttu-id="c2f7d-116">Laflamme, C. Miquel, J. P.</span><span class="sxs-lookup"><span data-stu-id="c2f7d-116">Laflamme, C. Miquel, J. P.</span></span> <span data-ttu-id="c2f7d-117">Paz und W. H.</span><span class="sxs-lookup"><span data-stu-id="c2f7d-117">Paz and W. H.</span></span> <span data-ttu-id="c2f7d-118">Zurek, "Perfect Quantum Error Korrektur Code", "Phys. Rev. Lett.</span><span class="sxs-lookup"><span data-stu-id="c2f7d-118">Zurek, "Perfect quantum error correction code," Phys. Rev. Lett.</span></span> <span data-ttu-id="c2f7d-119">77 (1996) PP. 198-201; https://arxiv.org/abs/quant-ph/9602019</span><span class="sxs-lookup"><span data-stu-id="c2f7d-119">77 (1996) pp. 198-201; https://arxiv.org/abs/quant-ph/9602019</span></span>
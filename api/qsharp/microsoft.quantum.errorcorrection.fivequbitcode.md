---
uid: Microsoft.Quantum.ErrorCorrection.FiveQubitCode
title: "\"Fvequbitcode\"-Funktion"
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: FiveQubitCode
qsharp.summary: Returns a QECC value representing the ⟦5, 1, 3⟧ code encoder and decoder with in-place syndrome measurement.
ms.openlocfilehash: 540dcf1eafa7449f386676a9a3c9562a4d4bf29c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853137"
---
# <a name="fivequbitcode-function"></a><span data-ttu-id="29cfa-102">"Fvequbitcode"-Funktion</span><span class="sxs-lookup"><span data-stu-id="29cfa-102">FiveQubitCode function</span></span>

<span data-ttu-id="29cfa-103">Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="29cfa-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="29cfa-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="29cfa-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="29cfa-105">Gibt einen qecc-Wert zurück, der den ⟦ 5, 1, 3 ⟧ Code Encoder und den Decoder mit der direkten Messung darstellt.</span><span class="sxs-lookup"><span data-stu-id="29cfa-105">Returns a QECC value representing the ⟦5, 1, 3⟧ code encoder and decoder with in-place syndrome measurement.</span></span>

```qsharp
function FiveQubitCode () : Microsoft.Quantum.ErrorCorrection.QECC
```


## <a name="output--qecc"></a><span data-ttu-id="29cfa-106">Ausgabe: [qecc](xref:Microsoft.Quantum.ErrorCorrection.QECC)</span><span class="sxs-lookup"><span data-stu-id="29cfa-106">Output : [QECC](xref:Microsoft.Quantum.ErrorCorrection.QECC)</span></span>

<span data-ttu-id="29cfa-107">Gibt eine Implementierung eines Quantum-Fehlerkorrekturcodes zurück, indem ein-Typ angegeben wird `QECC` .</span><span class="sxs-lookup"><span data-stu-id="29cfa-107">Returns an implementation of a quantum error correction code by specifying a `QECC` type.</span></span>

## <a name="remarks"></a><span data-ttu-id="29cfa-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="29cfa-108">Remarks</span></span>

<span data-ttu-id="29cfa-109">Dieser Code wurde in den folgenden zwei Dokumenten unabhängig voneinander gefunden:</span><span class="sxs-lookup"><span data-stu-id="29cfa-109">This code was found independently in the following two papers:</span></span>

- <span data-ttu-id="29cfa-110">C.</span><span class="sxs-lookup"><span data-stu-id="29cfa-110">C.</span></span> <span data-ttu-id="29cfa-111">H.</span><span class="sxs-lookup"><span data-stu-id="29cfa-111">H.</span></span> <span data-ttu-id="29cfa-112">Bennett, D. divincenzo, J. A.</span><span class="sxs-lookup"><span data-stu-id="29cfa-112">Bennett, D. DiVincenzo, J. A.</span></span> <span data-ttu-id="29cfa-113">Smolin und W. K.</span><span class="sxs-lookup"><span data-stu-id="29cfa-113">Smolin and W. K.</span></span> <span data-ttu-id="29cfa-114">Wootters, "gemischte Zustands jede Verflechtungen und Quantum-Fehlerkorrektur", "Phys. Rev. A, 54 (1996) PP. 3824-3851; https://arxiv.org/abs/quant-ph/9604024 und</span><span class="sxs-lookup"><span data-stu-id="29cfa-114">Wootters, "Mixed state entanglement and quantum error correction," Phys. Rev. A, 54 (1996) pp. 3824-3851; https://arxiv.org/abs/quant-ph/9604024 and</span></span>
- <span data-ttu-id="29cfa-115">R.</span><span class="sxs-lookup"><span data-stu-id="29cfa-115">R.</span></span> <span data-ttu-id="29cfa-116">Laflamme, C. Miquel, J. P.</span><span class="sxs-lookup"><span data-stu-id="29cfa-116">Laflamme, C. Miquel, J. P.</span></span> <span data-ttu-id="29cfa-117">Paz und W. H.</span><span class="sxs-lookup"><span data-stu-id="29cfa-117">Paz and W. H.</span></span> <span data-ttu-id="29cfa-118">Zurek, "Perfect Quantum Error Korrektur Code", "Phys. Rev. Lett.</span><span class="sxs-lookup"><span data-stu-id="29cfa-118">Zurek, "Perfect quantum error correction code," Phys. Rev. Lett.</span></span> <span data-ttu-id="29cfa-119">77 (1996) PP. 198-201; https://arxiv.org/abs/quant-ph/9602019</span><span class="sxs-lookup"><span data-stu-id="29cfa-119">77 (1996) pp. 198-201; https://arxiv.org/abs/quant-ph/9602019</span></span>
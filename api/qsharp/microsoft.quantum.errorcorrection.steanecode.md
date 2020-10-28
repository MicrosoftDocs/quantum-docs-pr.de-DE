---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCode
title: Steanäcode-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCode
qsharp.summary: Returns a CSS value representing the ⟦7, 1, 3⟧ Steane code encoder and decoder with in-place syndrome measurement.
ms.openlocfilehash: ea36320fff1f0c24426e2fcead976ef051d6699f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702414"
---
# <a name="steanecode-function"></a><span data-ttu-id="986e3-102">Steanäcode-Funktion</span><span class="sxs-lookup"><span data-stu-id="986e3-102">SteaneCode function</span></span>

<span data-ttu-id="986e3-103">Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="986e3-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="986e3-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="986e3-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="986e3-105">Gibt einen CSS-Wert zurück, der den ⟦ 7, 1, 3 ⟧ Steane-Code Encoder und den Decoder mit der direkten Messung darstellt.</span><span class="sxs-lookup"><span data-stu-id="986e3-105">Returns a CSS value representing the ⟦7, 1, 3⟧ Steane code encoder and decoder with in-place syndrome measurement.</span></span>

```qsharp
function SteaneCode () : Microsoft.Quantum.ErrorCorrection.CSS
```


## <a name="output--css"></a><span data-ttu-id="986e3-106">Ausgabe: [CSS](xref:Microsoft.Quantum.ErrorCorrection.CSS)</span><span class="sxs-lookup"><span data-stu-id="986e3-106">Output : [CSS](xref:Microsoft.Quantum.ErrorCorrection.CSS)</span></span>

<span data-ttu-id="986e3-107">Ein Objekt vom Typ CSS, das alle relevanten Daten sammelt, um die Codierung und Fehlerkorrektur für den ⟦ 7, 1, 3 ⟧ Steane-Code auszuführen.</span><span class="sxs-lookup"><span data-stu-id="986e3-107">An object of CSS type which collects all relevant data to perform encoding and error correction for the ⟦7, 1, 3⟧ Steane code.</span></span>

## <a name="remarks"></a><span data-ttu-id="986e3-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="986e3-108">Remarks</span></span>

<span data-ttu-id="986e3-109">Diesen Code finden Sie im folgenden Artikel:</span><span class="sxs-lookup"><span data-stu-id="986e3-109">This code was found in the following paper:</span></span>

- <span data-ttu-id="986e3-110">A.</span><span class="sxs-lookup"><span data-stu-id="986e3-110">A.</span></span> <span data-ttu-id="986e3-111">Steane, "mehrfache Partikel Störungen und Quantum-Fehlerkorrektur", proc.</span><span class="sxs-lookup"><span data-stu-id="986e3-111">Steane, "Multiple Particle Interference and Quantum Error Correction", Proc.</span></span> <span data-ttu-id="986e3-112">Stammt.</span><span class="sxs-lookup"><span data-stu-id="986e3-112">Roy.</span></span> <span data-ttu-id="986e3-113">Soc. Lond.</span><span class="sxs-lookup"><span data-stu-id="986e3-113">Soc. Lond.</span></span> <span data-ttu-id="986e3-114">A452 (1996) PP. 2551; https://arxiv.org/abs/quant-ph/9601029.</span><span class="sxs-lookup"><span data-stu-id="986e3-114">A452 (1996) pp. 2551; https://arxiv.org/abs/quant-ph/9601029.</span></span>
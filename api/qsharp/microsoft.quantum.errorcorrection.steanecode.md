---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCode
title: Steanäcode-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCode
qsharp.summary: Returns a CSS value representing the ⟦7, 1, 3⟧ Steane code encoder and decoder with in-place syndrome measurement.
ms.openlocfilehash: b981c82acfa82cd58d82666703d4bb95ac5df280
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200474"
---
# <a name="steanecode-function"></a><span data-ttu-id="937d4-102">Steanäcode-Funktion</span><span class="sxs-lookup"><span data-stu-id="937d4-102">SteaneCode function</span></span>

<span data-ttu-id="937d4-103">Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="937d4-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="937d4-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="937d4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="937d4-105">Gibt einen CSS-Wert zurück, der den ⟦ 7, 1, 3 ⟧ Steane-Code Encoder und den Decoder mit der direkten Messung darstellt.</span><span class="sxs-lookup"><span data-stu-id="937d4-105">Returns a CSS value representing the ⟦7, 1, 3⟧ Steane code encoder and decoder with in-place syndrome measurement.</span></span>

```qsharp
function SteaneCode () : Microsoft.Quantum.ErrorCorrection.CSS
```


## <a name="output--css"></a><span data-ttu-id="937d4-106">Ausgabe: [CSS](xref:Microsoft.Quantum.ErrorCorrection.CSS)</span><span class="sxs-lookup"><span data-stu-id="937d4-106">Output : [CSS](xref:Microsoft.Quantum.ErrorCorrection.CSS)</span></span>

<span data-ttu-id="937d4-107">Ein Objekt vom Typ CSS, das alle relevanten Daten sammelt, um die Codierung und Fehlerkorrektur für den ⟦ 7, 1, 3 ⟧ Steane-Code auszuführen.</span><span class="sxs-lookup"><span data-stu-id="937d4-107">An object of CSS type which collects all relevant data to perform encoding and error correction for the ⟦7, 1, 3⟧ Steane code.</span></span>

## <a name="remarks"></a><span data-ttu-id="937d4-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="937d4-108">Remarks</span></span>

<span data-ttu-id="937d4-109">Diesen Code finden Sie im folgenden Artikel:</span><span class="sxs-lookup"><span data-stu-id="937d4-109">This code was found in the following paper:</span></span>

- <span data-ttu-id="937d4-110">A.</span><span class="sxs-lookup"><span data-stu-id="937d4-110">A.</span></span> <span data-ttu-id="937d4-111">Steane, "mehrfache Partikel Störungen und Quantum-Fehlerkorrektur", proc.</span><span class="sxs-lookup"><span data-stu-id="937d4-111">Steane, "Multiple Particle Interference and Quantum Error Correction", Proc.</span></span> <span data-ttu-id="937d4-112">Stammt.</span><span class="sxs-lookup"><span data-stu-id="937d4-112">Roy.</span></span> <span data-ttu-id="937d4-113">Soc. Lond.</span><span class="sxs-lookup"><span data-stu-id="937d4-113">Soc. Lond.</span></span> <span data-ttu-id="937d4-114">A452 (1996) PP. 2551; https://arxiv.org/abs/quant-ph/9601029.</span><span class="sxs-lookup"><span data-stu-id="937d4-114">A452 (1996) pp. 2551; https://arxiv.org/abs/quant-ph/9601029.</span></span>
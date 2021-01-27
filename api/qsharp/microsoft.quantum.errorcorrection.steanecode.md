---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCode
title: Steanäcode-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCode
qsharp.summary: Returns a CSS value representing the ⟦7, 1, 3⟧ Steane code encoder and decoder with in-place syndrome measurement.
ms.openlocfilehash: af3f3ef5088b898bd827ebca00fdc7fcb992f2a1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853052"
---
# <a name="steanecode-function"></a><span data-ttu-id="654c3-102">Steanäcode-Funktion</span><span class="sxs-lookup"><span data-stu-id="654c3-102">SteaneCode function</span></span>

<span data-ttu-id="654c3-103">Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="654c3-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="654c3-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="654c3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="654c3-105">Gibt einen CSS-Wert zurück, der den ⟦ 7, 1, 3 ⟧ Steane-Code Encoder und den Decoder mit der direkten Messung darstellt.</span><span class="sxs-lookup"><span data-stu-id="654c3-105">Returns a CSS value representing the ⟦7, 1, 3⟧ Steane code encoder and decoder with in-place syndrome measurement.</span></span>

```qsharp
function SteaneCode () : Microsoft.Quantum.ErrorCorrection.CSS
```


## <a name="output--css"></a><span data-ttu-id="654c3-106">Ausgabe: [CSS](xref:Microsoft.Quantum.ErrorCorrection.CSS)</span><span class="sxs-lookup"><span data-stu-id="654c3-106">Output : [CSS](xref:Microsoft.Quantum.ErrorCorrection.CSS)</span></span>

<span data-ttu-id="654c3-107">Ein Objekt vom Typ CSS, das alle relevanten Daten sammelt, um die Codierung und Fehlerkorrektur für den ⟦ 7, 1, 3 ⟧ Steane-Code auszuführen.</span><span class="sxs-lookup"><span data-stu-id="654c3-107">An object of CSS type which collects all relevant data to perform encoding and error correction for the ⟦7, 1, 3⟧ Steane code.</span></span>

## <a name="remarks"></a><span data-ttu-id="654c3-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="654c3-108">Remarks</span></span>

<span data-ttu-id="654c3-109">Diesen Code finden Sie im folgenden Artikel:</span><span class="sxs-lookup"><span data-stu-id="654c3-109">This code was found in the following paper:</span></span>

- <span data-ttu-id="654c3-110">A.</span><span class="sxs-lookup"><span data-stu-id="654c3-110">A.</span></span> <span data-ttu-id="654c3-111">Steane, "mehrfache Partikel Störungen und Quantum-Fehlerkorrektur", proc.</span><span class="sxs-lookup"><span data-stu-id="654c3-111">Steane, "Multiple Particle Interference and Quantum Error Correction", Proc.</span></span> <span data-ttu-id="654c3-112">Stammt.</span><span class="sxs-lookup"><span data-stu-id="654c3-112">Roy.</span></span> <span data-ttu-id="654c3-113">Soc. Lond.</span><span class="sxs-lookup"><span data-stu-id="654c3-113">Soc. Lond.</span></span> <span data-ttu-id="654c3-114">A452 (1996) PP. 2551; https://arxiv.org/abs/quant-ph/9601029.</span><span class="sxs-lookup"><span data-stu-id="654c3-114">A452 (1996) pp. 2551; https://arxiv.org/abs/quant-ph/9601029.</span></span>
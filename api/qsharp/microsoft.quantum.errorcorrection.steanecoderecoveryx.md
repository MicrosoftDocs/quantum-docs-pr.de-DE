---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX
title: Steanecoderecoveryx-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCodeRecoveryX
qsharp.summary: Decoder for the X-part of the stabilizer group of the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: c90eac291ebe718d10377399184ad705bb51673e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98824697"
---
# <a name="steanecoderecoveryx-function"></a><span data-ttu-id="40543-102">Steanecoderecoveryx-Funktion</span><span class="sxs-lookup"><span data-stu-id="40543-102">SteaneCodeRecoveryX function</span></span>

<span data-ttu-id="40543-103">Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="40543-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="40543-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="40543-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="40543-105">Decoder für den X-Teil der stabilikostabilisgruppe des ⟦ 7, 1, 3 ⟧ Steane Quantum-Codes.</span><span class="sxs-lookup"><span data-stu-id="40543-105">Decoder for the X-part of the stabilizer group of the ⟦7, 1, 3⟧ Steane quantum code.</span></span>

```qsharp
function SteaneCodeRecoveryX (syndrome : Microsoft.Quantum.ErrorCorrection.Syndrome) : Pauli[]
```


## <a name="input"></a><span data-ttu-id="40543-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="40543-106">Input</span></span>

### <a name="syndrome--syndrome"></a><span data-ttu-id="40543-107">-Syndrom:- [Syndrom](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)</span><span class="sxs-lookup"><span data-stu-id="40543-107">syndrome : [Syndrome](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)</span></span>

<span data-ttu-id="40543-108">Ein von der Messung des X-Teils des Stabilisators erteiles-Syndrom-Array.</span><span class="sxs-lookup"><span data-stu-id="40543-108">A syndrome array obtained from measuring the X-part of the stabilizer.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="40543-109">Ausgabe: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="40543-109">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="40543-110">Ein Array von Pauli-Vorgängen, das bei Anwendung auf das codierte Quantum-System den Fehler korrigiert, der entspricht `syndrome` .</span><span class="sxs-lookup"><span data-stu-id="40543-110">An array of Pauli operations which, when applied to the encoded quantum system corrects the error corresponding to `syndrome`.</span></span>

## <a name="remarks"></a><span data-ttu-id="40543-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="40543-111">Remarks</span></span>

<span data-ttu-id="40543-112">Der ausgewählte Decoder verwendet die CSS-Code Eigenschaft des ⟦ 7, 1, 3 ⟧ Steane-Codes, d. h., er korrigiert X-Fehler und Z-Fehler separat.</span><span class="sxs-lookup"><span data-stu-id="40543-112">The chosen decoder uses the CSS code property of the ⟦7, 1, 3⟧ Steane code, i.e., it corrects X errors and Z errors separately.</span></span> <span data-ttu-id="40543-113">Eine Eigenschaft des Codes besteht darin, dass der Speicherort der x-und z-Korrektur, die angewendet werden soll, die 3-Bit-Codierung des x-bzw. z-syndrotes ist, wenn es sich um eine ganze Zahl handelt.</span><span class="sxs-lookup"><span data-stu-id="40543-113">A property of the code is that the location of the X, respectively, Z correction to be applied is the 3-bit encoding of the X, respectively, Z syndrome when considered an integer.</span></span>

## <a name="references"></a><span data-ttu-id="40543-114">References</span><span class="sxs-lookup"><span data-stu-id="40543-114">References</span></span>

- <span data-ttu-id="40543-115">D:</span><span class="sxs-lookup"><span data-stu-id="40543-115">D.</span></span> <span data-ttu-id="40543-116">Gottesman, "Stabilisator Codes und Quantum Error Korrektur", "Ph.D. Thesis, Caltech, 1997; https://arxiv.org/abs/quant-ph/9705052</span><span class="sxs-lookup"><span data-stu-id="40543-116">Gottesman, "Stabilizer Codes and Quantum Error Correction," Ph.D. Thesis, Caltech, 1997; https://arxiv.org/abs/quant-ph/9705052</span></span>

## <a name="see-also"></a><span data-ttu-id="40543-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="40543-117">See Also</span></span>

- [<span data-ttu-id="40543-118">Microsoft. Quantum. errorcorrection. steanecoderecoveryx</span><span class="sxs-lookup"><span data-stu-id="40543-118">Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX</span></span>](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX)
- [<span data-ttu-id="40543-119">Microsoft. Quantum. errorcorrection. steanecoderecoveryf</span><span class="sxs-lookup"><span data-stu-id="40543-119">Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryFns</span></span>](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryFns)
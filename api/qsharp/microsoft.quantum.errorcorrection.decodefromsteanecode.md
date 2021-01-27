---
uid: Microsoft.Quantum.ErrorCorrection.DecodeFromSteaneCode
title: Decodefromsteanäcode-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: DecodeFromSteaneCode
qsharp.summary: An inverse encoding operation that maps an unencoded quantum register to an encoded quantum register under the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: 54e47b65ed7a89c8ff9026126a9542d3d7ba15cc
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98827385"
---
# <a name="decodefromsteanecode-operation"></a><span data-ttu-id="887d6-102">Decodefromsteanäcode-Vorgang</span><span class="sxs-lookup"><span data-stu-id="887d6-102">DecodeFromSteaneCode operation</span></span>

<span data-ttu-id="887d6-103">Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="887d6-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="887d6-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="887d6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="887d6-105">Ein umgekehrter Codierungs Vorgang, der ein uncodiertes Quantum-Register einem codierten Quantum-Register unter dem Quantum-Code ⟦ 7, 1, 3 ⟧ Steane zuordnet.</span><span class="sxs-lookup"><span data-stu-id="887d6-105">An inverse encoding operation that maps an unencoded quantum register to an encoded quantum register under the ⟦7, 1, 3⟧ Steane quantum code.</span></span>

```qsharp
operation DecodeFromSteaneCode (logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : (Qubit[], Qubit[])
```


## <a name="input"></a><span data-ttu-id="887d6-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="887d6-106">Input</span></span>

### <a name="logicalregister--logicalregister"></a><span data-ttu-id="887d6-107">logicalregister: [logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="887d6-107">logicalRegister : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="887d6-108">Ein Array von Qubits, das den logischen Zustand des codierten 5-Qubit-Codes darstellt.</span><span class="sxs-lookup"><span data-stu-id="887d6-108">An array of qubits representing the encoded 5-qubit code logical state.</span></span>



## <a name="output--qubitqubit"></a><span data-ttu-id="887d6-109">Ausgabe: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[])</span><span class="sxs-lookup"><span data-stu-id="887d6-109">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[])</span></span>

<span data-ttu-id="887d6-110">Ein Qubit-Array der Länge 1, das den nicht codierten Zustand im ersten Parameter sowie zusätzliche Qubits im zweiten Parameter darstellt.</span><span class="sxs-lookup"><span data-stu-id="887d6-110">A qubit array of length 1 representing the unencoded state in the first parameter, together with auxiliary qubits in the second parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="887d6-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="887d6-111">Remarks</span></span>

<span data-ttu-id="887d6-112">Der ausgewählte Decoder verwendet die CSS-Code Eigenschaft des ⟦ 7, 1, 3 ⟧ Steane-Codes, d. h., er korrigiert X-Fehler und Z-Fehler separat.</span><span class="sxs-lookup"><span data-stu-id="887d6-112">The chosen decoder uses the CSS code property of the ⟦7, 1, 3⟧ Steane code, i.e., it corrects X errors and Z errors separately.</span></span> <span data-ttu-id="887d6-113">Eine Eigenschaft des Codes besteht darin, dass der Speicherort der x-und z-Korrektur, die angewendet werden soll, die 3-Bit-Codierung des x-bzw. z-syndrotes ist, wenn es sich um eine ganze Zahl handelt.</span><span class="sxs-lookup"><span data-stu-id="887d6-113">A property of the code is that the location of the X, respectively, Z correction to be applied is the 3-bit encoding of the X, respectively, Z syndrome when considered an integer.</span></span>

## <a name="references"></a><span data-ttu-id="887d6-114">References</span><span class="sxs-lookup"><span data-stu-id="887d6-114">References</span></span>

- <span data-ttu-id="887d6-115">D:</span><span class="sxs-lookup"><span data-stu-id="887d6-115">D.</span></span> <span data-ttu-id="887d6-116">Gottesman, "Stabilisator Codes und Quantum Error Korrektur", "Ph.D. Thesis, Caltech, 1997; https://arxiv.org/abs/quant-ph/9705052</span><span class="sxs-lookup"><span data-stu-id="887d6-116">Gottesman, "Stabilizer Codes and Quantum Error Correction," Ph.D. Thesis, Caltech, 1997; https://arxiv.org/abs/quant-ph/9705052</span></span>

## <a name="see-also"></a><span data-ttu-id="887d6-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="887d6-117">See Also</span></span>

- [<span data-ttu-id="887d6-118">Microsoft. Quantum. errorcorrection. steanecodebug</span><span class="sxs-lookup"><span data-stu-id="887d6-118">Microsoft.Quantum.ErrorCorrection.SteaneCodeEncoder</span></span>](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeEncoder)
- [<span data-ttu-id="887d6-119">Microsoft. Quantum. errorcorrection. steanecodecodecoder</span><span class="sxs-lookup"><span data-stu-id="887d6-119">Microsoft.Quantum.ErrorCorrection.SteaneCodeDecoder</span></span>](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeDecoder)
- [<span data-ttu-id="887d6-120">Microsoft. Quantum. errorcorrection. logicalregister</span><span class="sxs-lookup"><span data-stu-id="887d6-120">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
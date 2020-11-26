---
uid: Microsoft.Quantum.ErrorCorrection.DecodeFromBitFlipCode
title: Decodefrombitflipcode-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: DecodeFromBitFlipCode
qsharp.summary: Decodes from the [3, 1, 3] / ⟦3, 1, 1⟧ bit-flip code.
ms.openlocfilehash: 84cf83f24d02f261f1768e16390f83c9b294b759
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201154"
---
# <a name="decodefrombitflipcode-operation"></a><span data-ttu-id="6009c-102">Decodefrombitflipcode-Vorgang</span><span class="sxs-lookup"><span data-stu-id="6009c-102">DecodeFromBitFlipCode operation</span></span>

<span data-ttu-id="6009c-103">Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="6009c-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="6009c-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6009c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6009c-105">Decodiert aus dem [3, 1, 3]/⟦ 3, 1, 1 ⟧ Bit-Flip-Code.</span><span class="sxs-lookup"><span data-stu-id="6009c-105">Decodes from the [3, 1, 3] / ⟦3, 1, 1⟧ bit-flip code.</span></span>

```qsharp
operation DecodeFromBitFlipCode (logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : (Qubit[], Qubit[])
```


## <a name="input"></a><span data-ttu-id="6009c-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6009c-106">Input</span></span>

### <a name="logicalregister--logicalregister"></a><span data-ttu-id="6009c-107">logicalregister: [logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="6009c-107">logicalRegister : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="6009c-108">Ein Codeblock des Bit-Flip-Codes.</span><span class="sxs-lookup"><span data-stu-id="6009c-108">A code block of the bit-flip code.</span></span>



## <a name="output--qubitqubit"></a><span data-ttu-id="6009c-109">Ausgabe: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[])</span><span class="sxs-lookup"><span data-stu-id="6009c-109">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[])</span></span>

<span data-ttu-id="6009c-110">Ein Tupel der in das logische Register codierten Daten und die zusätzlichen Qubits, die für die Darstellung des-Syndroms verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6009c-110">A tuple of the data encoded into the logical register, and the auxiliary qubits used to represent the syndrome.</span></span>

## <a name="see-also"></a><span data-ttu-id="6009c-111">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6009c-111">See Also</span></span>

- [<span data-ttu-id="6009c-112">Microsoft. Quantum. errorcorrection. logicalregister</span><span class="sxs-lookup"><span data-stu-id="6009c-112">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
- [<span data-ttu-id="6009c-113">Microsoft. Quantum. errorcorrection. encodeindebitflipcode</span><span class="sxs-lookup"><span data-stu-id="6009c-113">Microsoft.Quantum.ErrorCorrection.EncodeIntoBitFlipCode</span></span>](xref:Microsoft.Quantum.ErrorCorrection.EncodeIntoBitFlipCode)
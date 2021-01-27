---
uid: Microsoft.Quantum.ErrorCorrection.DecodeFromBitFlipCode
title: Decodefrombitflipcode-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: DecodeFromBitFlipCode
qsharp.summary: Decodes from the [3, 1, 3] / ⟦3, 1, 1⟧ bit-flip code.
ms.openlocfilehash: b16e84340053b6c1eab7b91ed8db0461b9eac98e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98827565"
---
# <a name="decodefrombitflipcode-operation"></a><span data-ttu-id="7fc25-102">Decodefrombitflipcode-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7fc25-102">DecodeFromBitFlipCode operation</span></span>

<span data-ttu-id="7fc25-103">Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="7fc25-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="7fc25-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7fc25-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7fc25-105">Decodiert aus dem [3, 1, 3]/⟦ 3, 1, 1 ⟧ Bit-Flip-Code.</span><span class="sxs-lookup"><span data-stu-id="7fc25-105">Decodes from the [3, 1, 3] / ⟦3, 1, 1⟧ bit-flip code.</span></span>

```qsharp
operation DecodeFromBitFlipCode (logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : (Qubit[], Qubit[])
```


## <a name="input"></a><span data-ttu-id="7fc25-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7fc25-106">Input</span></span>

### <a name="logicalregister--logicalregister"></a><span data-ttu-id="7fc25-107">logicalregister: [logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="7fc25-107">logicalRegister : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="7fc25-108">Ein Codeblock des Bit-Flip-Codes.</span><span class="sxs-lookup"><span data-stu-id="7fc25-108">A code block of the bit-flip code.</span></span>



## <a name="output--qubitqubit"></a><span data-ttu-id="7fc25-109">Ausgabe: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[])</span><span class="sxs-lookup"><span data-stu-id="7fc25-109">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[])</span></span>

<span data-ttu-id="7fc25-110">Ein Tupel der in das logische Register codierten Daten und die zusätzlichen Qubits, die für die Darstellung des-Syndroms verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7fc25-110">A tuple of the data encoded into the logical register, and the auxiliary qubits used to represent the syndrome.</span></span>

## <a name="see-also"></a><span data-ttu-id="7fc25-111">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7fc25-111">See Also</span></span>

- [<span data-ttu-id="7fc25-112">Microsoft. Quantum. errorcorrection. logicalregister</span><span class="sxs-lookup"><span data-stu-id="7fc25-112">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
- [<span data-ttu-id="7fc25-113">Microsoft. Quantum. errorcorrection. encodeindebitflipcode</span><span class="sxs-lookup"><span data-stu-id="7fc25-113">Microsoft.Quantum.ErrorCorrection.EncodeIntoBitFlipCode</span></span>](xref:Microsoft.Quantum.ErrorCorrection.EncodeIntoBitFlipCode)
---
uid: Microsoft.Quantum.ErrorCorrection.EncodeIntoBitFlipCode
title: Encodeindebitflipcode-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeIntoBitFlipCode
qsharp.summary: Encodes into the [3, 1, 3] / ⟦3, 1, 1⟧ bit-flip code.
ms.openlocfilehash: b27759caba3c5dd363dbdf24d6e5de76870173cf
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200950"
---
# <a name="encodeintobitflipcode-operation"></a><span data-ttu-id="491d3-102">Encodeindebitflipcode-Vorgang</span><span class="sxs-lookup"><span data-stu-id="491d3-102">EncodeIntoBitFlipCode operation</span></span>

<span data-ttu-id="491d3-103">Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="491d3-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="491d3-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="491d3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="491d3-105">Codiert in den [3, 1, 3]/⟦ 3, 1, 1 ⟧ Bit-Flip-Code.</span><span class="sxs-lookup"><span data-stu-id="491d3-105">Encodes into the [3, 1, 3] / ⟦3, 1, 1⟧ bit-flip code.</span></span>

```qsharp
operation EncodeIntoBitFlipCode (physRegister : Qubit[], auxQubits : Qubit[]) : Microsoft.Quantum.ErrorCorrection.LogicalRegister
```


## <a name="input"></a><span data-ttu-id="491d3-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="491d3-106">Input</span></span>

### <a name="physregister--qubit"></a><span data-ttu-id="491d3-107">physregister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="491d3-107">physRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="491d3-108">Ein Register physischer Qubits, das die zu schützenden Daten darstellt.</span><span class="sxs-lookup"><span data-stu-id="491d3-108">A register of physical qubits representing the data to be protected.</span></span>


### <a name="auxqubits--qubit"></a><span data-ttu-id="491d3-109">"auxqubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]"</span><span class="sxs-lookup"><span data-stu-id="491d3-109">auxQubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="491d3-110">Ein Register von hilfsqubits, die anfänglich im $ \ket {00} $-Status verwendet werden, um die zu schützenden Daten zu codieren.</span><span class="sxs-lookup"><span data-stu-id="491d3-110">A register of auxiliary qubits initially in the $\ket{00}$ state to be used in encoding the data to be protected.</span></span>



## <a name="output--logicalregister"></a><span data-ttu-id="491d3-111">Ausgabe: [logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="491d3-111">Output : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="491d3-112">Die in der Codierung verwendeten physischen und zusätzlichen Qubits, die als logisches Register dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="491d3-112">The physical and auxiliary qubits used in encoding, represented as a logical register.</span></span>

## <a name="see-also"></a><span data-ttu-id="491d3-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="491d3-113">See Also</span></span>

- [<span data-ttu-id="491d3-114">Microsoft. Quantum. errorcorrection. logicalregister</span><span class="sxs-lookup"><span data-stu-id="491d3-114">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
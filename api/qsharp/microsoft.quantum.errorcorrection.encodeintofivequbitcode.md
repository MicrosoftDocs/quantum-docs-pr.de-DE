---
uid: Microsoft.Quantum.ErrorCorrection.EncodeIntoFiveQubitCode
title: Encodeindemevequbitcode-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeIntoFiveQubitCode
qsharp.summary: Encodes into the ⟦5, 1, 3⟧ quantum code.
ms.openlocfilehash: 1bccf46453ad34199dcebc5bcff693359fe2254c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98826323"
---
# <a name="encodeintofivequbitcode-operation"></a><span data-ttu-id="33e4b-102">Encodeindemevequbitcode-Vorgang</span><span class="sxs-lookup"><span data-stu-id="33e4b-102">EncodeIntoFiveQubitCode operation</span></span>

<span data-ttu-id="33e4b-103">Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="33e4b-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="33e4b-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="33e4b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="33e4b-105">Codiert in den ⟦ 5, 1, 3 ⟧ Quantum-Code.</span><span class="sxs-lookup"><span data-stu-id="33e4b-105">Encodes into the ⟦5, 1, 3⟧ quantum code.</span></span>

```qsharp
operation EncodeIntoFiveQubitCode (physRegister : Qubit[], auxQubits : Qubit[]) : Microsoft.Quantum.ErrorCorrection.LogicalRegister
```


## <a name="input"></a><span data-ttu-id="33e4b-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="33e4b-106">Input</span></span>

### <a name="physregister--qubit"></a><span data-ttu-id="33e4b-107">physregister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="33e4b-107">physRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="33e4b-108">Ein Qubit, das einen nicht codierten Zustand darstellt.</span><span class="sxs-lookup"><span data-stu-id="33e4b-108">A qubit representing an unencoded state.</span></span> <span data-ttu-id="33e4b-109">Dieses Array hat die `Qubit[]` Länge 1.</span><span class="sxs-lookup"><span data-stu-id="33e4b-109">This array `Qubit[]` is of length 1.</span></span>


### <a name="auxqubits--qubit"></a><span data-ttu-id="33e4b-110">"auxqubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]"</span><span class="sxs-lookup"><span data-stu-id="33e4b-110">auxQubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="33e4b-111">Ein Register von hilfsqubits, die zur Darstellung des codierten Zustands verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="33e4b-111">A register of auxiliary qubits that will be used to represent the encoded state.</span></span>



## <a name="output--logicalregister"></a><span data-ttu-id="33e4b-112">Ausgabe: [logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="33e4b-112">Output : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="33e4b-113">Ein Array physischer Qubits vom Typ `LogicalRegister` , das den codierten Zustand speichert.</span><span class="sxs-lookup"><span data-stu-id="33e4b-113">An array of physical qubits of type `LogicalRegister` that store the encoded state.</span></span>

## <a name="see-also"></a><span data-ttu-id="33e4b-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="33e4b-114">See Also</span></span>

- [<span data-ttu-id="33e4b-115">Microsoft. Quantum. errorcorrection. logicalregister</span><span class="sxs-lookup"><span data-stu-id="33e4b-115">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
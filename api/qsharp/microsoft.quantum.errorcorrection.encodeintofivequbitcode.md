---
uid: Microsoft.Quantum.ErrorCorrection.EncodeIntoFiveQubitCode
title: Encodeindemevequbitcode-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeIntoFiveQubitCode
qsharp.summary: Encodes into the ⟦5, 1, 3⟧ quantum code.
ms.openlocfilehash: c9df4c5c98a78cae8b3af4597020d35469454153
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702509"
---
# <a name="encodeintofivequbitcode-operation"></a><span data-ttu-id="1741f-102">Encodeindemevequbitcode-Vorgang</span><span class="sxs-lookup"><span data-stu-id="1741f-102">EncodeIntoFiveQubitCode operation</span></span>

<span data-ttu-id="1741f-103">Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="1741f-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="1741f-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1741f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="1741f-105">Codiert in den ⟦ 5, 1, 3 ⟧ Quantum-Code.</span><span class="sxs-lookup"><span data-stu-id="1741f-105">Encodes into the ⟦5, 1, 3⟧ quantum code.</span></span>

```qsharp
operation EncodeIntoFiveQubitCode (physRegister : Qubit[], auxQubits : Qubit[]) : Microsoft.Quantum.ErrorCorrection.LogicalRegister
```


## <a name="input"></a><span data-ttu-id="1741f-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1741f-106">Input</span></span>

### <a name="physregister--qubit"></a><span data-ttu-id="1741f-107">physregister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="1741f-107">physRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="1741f-108">Ein Qubit, das einen nicht codierten Zustand darstellt.</span><span class="sxs-lookup"><span data-stu-id="1741f-108">A qubit representing an unencoded state.</span></span> <span data-ttu-id="1741f-109">Dieses Array hat die `Qubit[]` Länge 1.</span><span class="sxs-lookup"><span data-stu-id="1741f-109">This array `Qubit[]` is of length 1.</span></span>


### <a name="auxqubits--qubit"></a><span data-ttu-id="1741f-110">"auxqubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]"</span><span class="sxs-lookup"><span data-stu-id="1741f-110">auxQubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="1741f-111">Ein Register von hilfsqubits, die zur Darstellung des codierten Zustands verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1741f-111">A register of auxiliary qubits that will be used to represent the encoded state.</span></span>



## <a name="output--logicalregister"></a><span data-ttu-id="1741f-112">Ausgabe: [logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="1741f-112">Output : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="1741f-113">Ein Array physischer Qubits vom Typ `LogicalRegister` , das den codierten Zustand speichert.</span><span class="sxs-lookup"><span data-stu-id="1741f-113">An array of physical qubits of type `LogicalRegister` that store the encoded state.</span></span>

## <a name="see-also"></a><span data-ttu-id="1741f-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1741f-114">See Also</span></span>

- [<span data-ttu-id="1741f-115">Microsoft. Quantum. errorcorrection. logicalregister</span><span class="sxs-lookup"><span data-stu-id="1741f-115">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
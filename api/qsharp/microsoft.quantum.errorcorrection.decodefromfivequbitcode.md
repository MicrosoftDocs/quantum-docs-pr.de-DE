---
uid: Microsoft.Quantum.ErrorCorrection.DecodeFromFiveQubitCode
title: Decodefrommevequbitcode-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: DecodeFromFiveQubitCode
qsharp.summary: Decodes the ⟦5, 1, 3⟧ quantum code.
ms.openlocfilehash: 9b4580cb88f03a16e3c9c55511d0ec5968cc636f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853167"
---
# <a name="decodefromfivequbitcode-operation"></a><span data-ttu-id="c7d1c-102">Decodefrommevequbitcode-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c7d1c-102">DecodeFromFiveQubitCode operation</span></span>

<span data-ttu-id="c7d1c-103">Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="c7d1c-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="c7d1c-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c7d1c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c7d1c-105">Decodiert den ⟦ 5, 1, 3 ⟧ Quantum-Code.</span><span class="sxs-lookup"><span data-stu-id="c7d1c-105">Decodes the ⟦5, 1, 3⟧ quantum code.</span></span>

```qsharp
operation DecodeFromFiveQubitCode (logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : (Qubit[], Qubit[])
```


## <a name="input"></a><span data-ttu-id="c7d1c-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c7d1c-106">Input</span></span>

### <a name="logicalregister--logicalregister"></a><span data-ttu-id="c7d1c-107">logicalregister: [logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="c7d1c-107">logicalRegister : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="c7d1c-108">Ein Array von Qubits, das den logischen Zustand des codierten 5-Qubit-Codes darstellt.</span><span class="sxs-lookup"><span data-stu-id="c7d1c-108">An array of qubits representing the encoded 5-qubit code logical state.</span></span>



## <a name="output--qubitqubit"></a><span data-ttu-id="c7d1c-109">Ausgabe: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[])</span><span class="sxs-lookup"><span data-stu-id="c7d1c-109">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[])</span></span>

<span data-ttu-id="c7d1c-110">Ein Qubit-Array der Länge 1, das den nicht codierten Zustand im ersten Parameter sowie zusätzliche Qubits im zweiten Parameter darstellt.</span><span class="sxs-lookup"><span data-stu-id="c7d1c-110">A qubit array of length 1 representing the unencoded state in the first parameter, together with auxiliary qubits in the second parameter.</span></span>

## <a name="see-also"></a><span data-ttu-id="c7d1c-111">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c7d1c-111">See Also</span></span>

- [<span data-ttu-id="c7d1c-112">Microsoft. Quantum. errorcorrection. fvequbitcodeencoder</span><span class="sxs-lookup"><span data-stu-id="c7d1c-112">Microsoft.Quantum.ErrorCorrection.FiveQubitCodeEncoder</span></span>](xref:Microsoft.Quantum.ErrorCorrection.FiveQubitCodeEncoder)
- [<span data-ttu-id="c7d1c-113">Microsoft. Quantum. errorcorrection. logicalregister</span><span class="sxs-lookup"><span data-stu-id="c7d1c-113">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
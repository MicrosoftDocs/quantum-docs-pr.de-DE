---
uid: Microsoft.Quantum.ErrorCorrection.SyndromeMeasOp
title: Benutzerdefinierter Typ "Syndrome-measop"
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SyndromeMeasOp
qsharp.summary: Represents an operation that is used to measure the syndrome of an error-correcting code block.
ms.openlocfilehash: 36336f9e47e5f360cf5e19ffb6e15b4af88b2580
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850049"
---
# <a name="syndromemeasop-user-defined-type"></a><span data-ttu-id="590ea-102">Benutzerdefinierter Typ "Syndrome-measop"</span><span class="sxs-lookup"><span data-stu-id="590ea-102">SyndromeMeasOp user defined type</span></span>

<span data-ttu-id="590ea-103">Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="590ea-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="590ea-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="590ea-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="590ea-105">Stellt einen Vorgang dar, der verwendet wird, um das-Syndrom eines Code Blocks mit Fehlerbehebung zu messen.</span><span class="sxs-lookup"><span data-stu-id="590ea-105">Represents an operation that is used to measure the syndrome of an error-correcting code block.</span></span>

```qsharp

newtype SyndromeMeasOp = ((Microsoft.Quantum.ErrorCorrection.LogicalRegister => Microsoft.Quantum.ErrorCorrection.Syndrome));
```



## <a name="example"></a><span data-ttu-id="590ea-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="590ea-106">Example</span></span>

<span data-ttu-id="590ea-107">Messen Sie die Syndrome für den Bit-Flip-Code $S = \langle ZZI, Izz \rangle $ using Scratch Qubits in nicht – Fault toleranter Weise:</span><span class="sxs-lookup"><span data-stu-id="590ea-107">Measure syndromes for the bit-flip code $S = \langle ZZI, IZZ \rangle$ using scratch qubits in a non–fault tolerant manner:</span></span>

```qsharp
    let syndMeasOp = SyndromeMeasOp(MeasureStabilizerGenerators([
            [PauliZ, PauliZ, PauliI],
            [PauliI, PauliZ, PauliZ]
        ], _, MeasureWithScratch));
```

## <a name="remarks"></a><span data-ttu-id="590ea-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="590ea-108">Remarks</span></span>

<span data-ttu-id="590ea-109">Die Signatur `(LogicalRegister => Syndrome)` stellt einen Vorgang dar, der gemeinsam mit den Qubits in `LogicalRegister` und einigen zusätzlichen Qubits gefolgt von einem Maß an zusätzlichen Qubits, um einen Wert zu extrahieren, `Syndrome` der die `Result[]` dieser Messungen darstellt.</span><span class="sxs-lookup"><span data-stu-id="590ea-109">The signature `(LogicalRegister => Syndrome)` represents an operation that acts jointly on the qubits in `LogicalRegister` and some auxiliary qubits followed by a measurements of the auxiliary qubits to extract a `Syndrome` value representing the `Result[]` of these measurements.</span></span>

## <a name="see-also"></a><span data-ttu-id="590ea-110">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="590ea-110">See Also</span></span>

- [<span data-ttu-id="590ea-111">Microsoft. Quantum. errorcorrection. logicalregister</span><span class="sxs-lookup"><span data-stu-id="590ea-111">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
- [<span data-ttu-id="590ea-112">Microsoft. Quantum. errorcorrection.-Syndrom</span><span class="sxs-lookup"><span data-stu-id="590ea-112">Microsoft.Quantum.ErrorCorrection.Syndrome</span></span>](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)
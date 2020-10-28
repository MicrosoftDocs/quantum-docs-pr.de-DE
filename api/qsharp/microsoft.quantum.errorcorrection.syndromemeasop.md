---
uid: Microsoft.Quantum.ErrorCorrection.SyndromeMeasOp
title: Benutzerdefinierter Typ "Syndrome-measop"
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SyndromeMeasOp
qsharp.summary: Represents an operation that is used to measure the syndrome of an error-correcting code block.
ms.openlocfilehash: 1314e16d26c7310bab21caa91cb398d4b6f09b29
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702389"
---
# <a name="syndromemeasop-user-defined-type"></a><span data-ttu-id="26f33-102">Benutzerdefinierter Typ "Syndrome-measop"</span><span class="sxs-lookup"><span data-stu-id="26f33-102">SyndromeMeasOp user defined type</span></span>

<span data-ttu-id="26f33-103">Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="26f33-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="26f33-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="26f33-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="26f33-105">Stellt einen Vorgang dar, der verwendet wird, um das-Syndrom eines Code Blocks mit Fehlerbehebung zu messen.</span><span class="sxs-lookup"><span data-stu-id="26f33-105">Represents an operation that is used to measure the syndrome of an error-correcting code block.</span></span>

```qsharp

newtype SyndromeMeasOp = ((Microsoft.Quantum.ErrorCorrection.LogicalRegister => Microsoft.Quantum.ErrorCorrection.Syndrome));
```



## <a name="remarks"></a><span data-ttu-id="26f33-106">Hinweise</span><span class="sxs-lookup"><span data-stu-id="26f33-106">Remarks</span></span>

<span data-ttu-id="26f33-107">Die Signatur `(LogicalRegister => Syndrome)` stellt einen Vorgang dar, der gemeinsam mit den Qubits in `LogicalRegister` und einigen zusätzlichen Qubits gefolgt von einem Maß an zusätzlichen Qubits, um einen Wert zu extrahieren, `Syndrome` der die `Result[]` dieser Messungen darstellt.</span><span class="sxs-lookup"><span data-stu-id="26f33-107">The signature `(LogicalRegister => Syndrome)` represents an operation that acts jointly on the qubits in `LogicalRegister` and some auxiliary qubits followed by a measurements of the auxiliary qubits to extract a `Syndrome` value representing the `Result[]` of these measurements.</span></span>

## <a name="see-also"></a><span data-ttu-id="26f33-108">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="26f33-108">See Also</span></span>

- [<span data-ttu-id="26f33-109">Microsoft. Quantum. errorcorrection. logicalregister</span><span class="sxs-lookup"><span data-stu-id="26f33-109">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
- [<span data-ttu-id="26f33-110">Microsoft. Quantum. errorcorrection.-Syndrom</span><span class="sxs-lookup"><span data-stu-id="26f33-110">Microsoft.Quantum.ErrorCorrection.Syndrome</span></span>](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)
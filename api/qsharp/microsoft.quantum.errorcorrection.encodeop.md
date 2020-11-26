---
uid: Microsoft.Quantum.ErrorCorrection.EncodeOp
title: Benutzerdefinierter encodeop-Typ
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeOp
qsharp.summary: >-
  Represents an operation which encodes a physical register into a logical register, using the provided scratch qubits.

  The first argument is taken to be the physical register that will be encoded, while the second argument is taken to be the scratch register that will be used.
ms.openlocfilehash: 18d6df6037b1fe66a171acea1936fcb9ba1b27e5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200899"
---
# <a name="encodeop-user-defined-type"></a><span data-ttu-id="9ef69-102">Benutzerdefinierter encodeop-Typ</span><span class="sxs-lookup"><span data-stu-id="9ef69-102">EncodeOp user defined type</span></span>

<span data-ttu-id="9ef69-103">Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="9ef69-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="9ef69-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9ef69-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9ef69-105">Stellt einen Vorgang dar, der ein physisches Register unter Verwendung der angegebenen Scratch-Qubits in ein logisches Register codiert.</span><span class="sxs-lookup"><span data-stu-id="9ef69-105">Represents an operation which encodes a physical register into a logical register, using the provided scratch qubits.</span></span>

<span data-ttu-id="9ef69-106">Bei dem ersten Argument handelt es sich um das physische Register, das codiert wird, während das zweite Argument als das zu verwendende Scratch-Register angenommen wird.</span><span class="sxs-lookup"><span data-stu-id="9ef69-106">The first argument is taken to be the physical register that will be encoded, while the second argument is taken to be the scratch register that will be used.</span></span>

```qsharp

newtype EncodeOp = (((Qubit[], Qubit[]) => Microsoft.Quantum.ErrorCorrection.LogicalRegister));
```


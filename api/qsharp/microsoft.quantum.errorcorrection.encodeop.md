---
uid: Microsoft.Quantum.ErrorCorrection.EncodeOp
title: Benutzerdefinierter encodeop-Typ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeOp
qsharp.summary: >-
  Represents an operation which encodes a physical register into a logical register, using the provided scratch qubits.

  The first argument is taken to be the physical register that will be encoded, while the second argument is taken to be the scratch register that will be used.
ms.openlocfilehash: da947cdc25cb0edd3a4144022bbfc6ecb84c647f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702486"
---
# <a name="encodeop-user-defined-type"></a>Benutzerdefinierter encodeop-Typ

Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)

Paketen [](https://nuget.org/packages/)


Stellt einen Vorgang dar, der ein physisches Register unter Verwendung der angegebenen Scratch-Qubits in ein logisches Register codiert.

Bei dem ersten Argument handelt es sich um das physische Register, das codiert wird, während das zweite Argument als das zu verwendende Scratch-Register angenommen wird.

```qsharp

newtype EncodeOp = (((Qubit[], Qubit[]) => Microsoft.Quantum.ErrorCorrection.LogicalRegister));
```


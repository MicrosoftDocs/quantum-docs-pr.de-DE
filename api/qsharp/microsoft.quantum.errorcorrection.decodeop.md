---
uid: Microsoft.Quantum.ErrorCorrection.DecodeOp
title: Decodeop-benutzerdefinierter Typ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: DecodeOp
qsharp.summary: >-
  Represents an operation which decodes an encoded register into a physical register and the scratch qubits used to record a syndrome.

  The argument to a DecodeOp is the same as the return from an EncodeOp, and vice versa.
ms.openlocfilehash: 0733ec016e50a320b162b111c7d87c32140fdacb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702515"
---
# <a name="decodeop-user-defined-type"></a>Decodeop-benutzerdefinierter Typ

Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)

Paketen [](https://nuget.org/packages/)


Stellt einen Vorgang dar, der ein codiertes Register in ein physisches Register und die für die Aufzeichnung eines-Syndroms verwendeten Scratch-Qubits decodiert.

Das Argument für einen decodeop ist mit dem Rückgabewert von encodeop identisch und umgekehrt.

```qsharp

newtype DecodeOp = ((Microsoft.Quantum.ErrorCorrection.LogicalRegister => (Qubit[], Qubit[])));
```


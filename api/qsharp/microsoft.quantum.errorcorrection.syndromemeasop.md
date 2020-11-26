---
uid: Microsoft.Quantum.ErrorCorrection.SyndromeMeasOp
title: Benutzerdefinierter Typ "Syndrome-measop"
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SyndromeMeasOp
qsharp.summary: Represents an operation that is used to measure the syndrome of an error-correcting code block.
ms.openlocfilehash: 65e47d82546b1df0beec2c00f435d3e7a28e6ae6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200253"
---
# <a name="syndromemeasop-user-defined-type"></a>Benutzerdefinierter Typ "Syndrome-measop"

Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Stellt einen Vorgang dar, der verwendet wird, um das-Syndrom eines Code Blocks mit Fehlerbehebung zu messen.

```qsharp

newtype SyndromeMeasOp = ((Microsoft.Quantum.ErrorCorrection.LogicalRegister => Microsoft.Quantum.ErrorCorrection.Syndrome));
```



## <a name="remarks"></a>Bemerkungen

Die Signatur `(LogicalRegister => Syndrome)` stellt einen Vorgang dar, der gemeinsam mit den Qubits in `LogicalRegister` und einigen zusätzlichen Qubits gefolgt von einem Maß an zusätzlichen Qubits, um einen Wert zu extrahieren, `Syndrome` der die `Result[]` dieser Messungen darstellt.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. errorcorrection. logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
- [Microsoft. Quantum. errorcorrection.-Syndrom](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)
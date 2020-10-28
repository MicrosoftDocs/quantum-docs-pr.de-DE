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
# <a name="syndromemeasop-user-defined-type"></a>Benutzerdefinierter Typ "Syndrome-measop"

Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)

Paketen [](https://nuget.org/packages/)


Stellt einen Vorgang dar, der verwendet wird, um das-Syndrom eines Code Blocks mit Fehlerbehebung zu messen.

```qsharp

newtype SyndromeMeasOp = ((Microsoft.Quantum.ErrorCorrection.LogicalRegister => Microsoft.Quantum.ErrorCorrection.Syndrome));
```



## <a name="remarks"></a>Hinweise

Die Signatur `(LogicalRegister => Syndrome)` stellt einen Vorgang dar, der gemeinsam mit den Qubits in `LogicalRegister` und einigen zusätzlichen Qubits gefolgt von einem Maß an zusätzlichen Qubits, um einen Wert zu extrahieren, `Syndrome` der die `Result[]` dieser Messungen darstellt.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. errorcorrection. logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
- [Microsoft. Quantum. errorcorrection.-Syndrom](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)
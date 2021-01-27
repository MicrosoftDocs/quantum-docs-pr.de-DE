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
# <a name="syndromemeasop-user-defined-type"></a>Benutzerdefinierter Typ "Syndrome-measop"

Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Stellt einen Vorgang dar, der verwendet wird, um das-Syndrom eines Code Blocks mit Fehlerbehebung zu messen.

```qsharp

newtype SyndromeMeasOp = ((Microsoft.Quantum.ErrorCorrection.LogicalRegister => Microsoft.Quantum.ErrorCorrection.Syndrome));
```



## <a name="example"></a>Beispiel

Messen Sie die Syndrome für den Bit-Flip-Code $S = \langle ZZI, Izz \rangle $ using Scratch Qubits in nicht – Fault toleranter Weise:

```qsharp
    let syndMeasOp = SyndromeMeasOp(MeasureStabilizerGenerators([
            [PauliZ, PauliZ, PauliI],
            [PauliI, PauliZ, PauliZ]
        ], _, MeasureWithScratch));
```

## <a name="remarks"></a>Bemerkungen

Die Signatur `(LogicalRegister => Syndrome)` stellt einen Vorgang dar, der gemeinsam mit den Qubits in `LogicalRegister` und einigen zusätzlichen Qubits gefolgt von einem Maß an zusätzlichen Qubits, um einen Wert zu extrahieren, `Syndrome` der die `Result[]` dieser Messungen darstellt.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. errorcorrection. logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
- [Microsoft. Quantum. errorcorrection.-Syndrom](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)
---
uid: Microsoft.Quantum.ErrorCorrection.EncodeIntoBitFlipCode
title: Encodeindebitflipcode-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeIntoBitFlipCode
qsharp.summary: Encodes into the [3, 1, 3] / ⟦3, 1, 1⟧ bit-flip code.
ms.openlocfilehash: 694d3f7a412b64b0ad533b4478a9274384d05c61
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702510"
---
# <a name="encodeintobitflipcode-operation"></a>Encodeindebitflipcode-Vorgang

Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)

Paketen [](https://nuget.org/packages/)


Codiert in den [3, 1, 3]/⟦ 3, 1, 1 ⟧ Bit-Flip-Code.

```qsharp
operation EncodeIntoBitFlipCode (physRegister : Qubit[], auxQubits : Qubit[]) : Microsoft.Quantum.ErrorCorrection.LogicalRegister
```


## <a name="input"></a>Eingabe

### <a name="physregister--qubit"></a>physregister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Ein Register physischer Qubits, das die zu schützenden Daten darstellt.


### <a name="auxqubits--qubit"></a>"auxqubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]"

Ein Register von hilfsqubits, die anfänglich im $ \ket {00} $-Status verwendet werden, um die zu schützenden Daten zu codieren.



## <a name="output--logicalregister"></a>Ausgabe: [logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)

Die in der Codierung verwendeten physischen und zusätzlichen Qubits, die als logisches Register dargestellt werden.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. errorcorrection. logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
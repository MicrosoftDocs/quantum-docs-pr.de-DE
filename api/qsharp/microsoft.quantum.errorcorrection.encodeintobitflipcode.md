---
uid: Microsoft.Quantum.ErrorCorrection.EncodeIntoBitFlipCode
title: Encodeindebitflipcode-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeIntoBitFlipCode
qsharp.summary: Encodes into the [3, 1, 3] / ⟦3, 1, 1⟧ bit-flip code.
ms.openlocfilehash: 44034a864c946a7d3dbb21bad5ee500660709f1a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98826676"
---
# <a name="encodeintobitflipcode-operation"></a>Encodeindebitflipcode-Vorgang

Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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
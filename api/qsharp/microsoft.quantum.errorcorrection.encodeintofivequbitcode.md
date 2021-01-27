---
uid: Microsoft.Quantum.ErrorCorrection.EncodeIntoFiveQubitCode
title: Encodeindemevequbitcode-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeIntoFiveQubitCode
qsharp.summary: Encodes into the ⟦5, 1, 3⟧ quantum code.
ms.openlocfilehash: 1bccf46453ad34199dcebc5bcff693359fe2254c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98826323"
---
# <a name="encodeintofivequbitcode-operation"></a>Encodeindemevequbitcode-Vorgang

Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Codiert in den ⟦ 5, 1, 3 ⟧ Quantum-Code.

```qsharp
operation EncodeIntoFiveQubitCode (physRegister : Qubit[], auxQubits : Qubit[]) : Microsoft.Quantum.ErrorCorrection.LogicalRegister
```


## <a name="input"></a>Eingabe

### <a name="physregister--qubit"></a>physregister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Ein Qubit, das einen nicht codierten Zustand darstellt. Dieses Array hat die `Qubit[]` Länge 1.


### <a name="auxqubits--qubit"></a>"auxqubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]"

Ein Register von hilfsqubits, die zur Darstellung des codierten Zustands verwendet werden.



## <a name="output--logicalregister"></a>Ausgabe: [logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)

Ein Array physischer Qubits vom Typ `LogicalRegister` , das den codierten Zustand speichert.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. errorcorrection. logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
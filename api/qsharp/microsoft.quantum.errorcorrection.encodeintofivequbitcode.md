---
uid: Microsoft.Quantum.ErrorCorrection.EncodeIntoFiveQubitCode
title: Encodeindemevequbitcode-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeIntoFiveQubitCode
qsharp.summary: Encodes into the ⟦5, 1, 3⟧ quantum code.
ms.openlocfilehash: c9df4c5c98a78cae8b3af4597020d35469454153
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702509"
---
# <a name="encodeintofivequbitcode-operation"></a>Encodeindemevequbitcode-Vorgang

Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)

Paketen [](https://nuget.org/packages/)


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
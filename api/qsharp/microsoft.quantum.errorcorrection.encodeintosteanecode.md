---
uid: Microsoft.Quantum.ErrorCorrection.EncodeIntoSteaneCode
title: Encodeindesteanecode-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeIntoSteaneCode
qsharp.summary: An encoding operation that maps an unencoded quantum register to an encoded quantum register under the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: 39b8ab549413d9d5281f6b84a6e970c45242fca8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702504"
---
# <a name="encodeintosteanecode-operation"></a>Encodeindesteanecode-Vorgang

Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)

Paketen [](https://nuget.org/packages/)


Ein Codierungs Vorgang, der ein uncodiertes Quantum-Register einem codierten Quantum-Register unter dem Quantum-Code ⟦ 7, 1, 3 ⟧ Steane zuordnet.

```qsharp
operation EncodeIntoSteaneCode (physRegister : Qubit[], auxQubits : Qubit[]) : Microsoft.Quantum.ErrorCorrection.LogicalRegister
```


## <a name="input"></a>Eingabe

### <a name="physregister--qubit"></a>physregister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Ein Qubit-Register, das den unverschlüsselten Quantenzustand enthält.


### <a name="auxqubits--qubit"></a>"auxqubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]"

Ein Qubit-Register, das anfänglich 0 (null) ist und dem Quantum-System hinzugefügt wird, sodass ein Codierungs Vorgang ausgeführt werden kann.



## <a name="output--logicalregister"></a>Ausgabe: [logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)

Ein Quantum-Register mit dem Zustand, nachdem der Steane-Encoder angewendet wurde.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. errorcorrection. logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
- [Microsoft. Quantum. errorcorrection. steanecodecodecoder](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeDecoder)
---
uid: Microsoft.Quantum.ErrorCorrection.DecodeFromBitFlipCode
title: Decodefrombitflipcode-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: DecodeFromBitFlipCode
qsharp.summary: Decodes from the [3, 1, 3] / ⟦3, 1, 1⟧ bit-flip code.
ms.openlocfilehash: be6ad5fce9eeb3eea031ff301b78dbb3680b66f0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702545"
---
# <a name="decodefrombitflipcode-operation"></a>Decodefrombitflipcode-Vorgang

Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)

Paketen [](https://nuget.org/packages/)


Decodiert aus dem [3, 1, 3]/⟦ 3, 1, 1 ⟧ Bit-Flip-Code.

```qsharp
operation DecodeFromBitFlipCode (logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : (Qubit[], Qubit[])
```


## <a name="input"></a>Eingabe

### <a name="logicalregister--logicalregister"></a>logicalregister: [logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)

Ein Codeblock des Bit-Flip-Codes.



## <a name="output--qubitqubit"></a>Ausgabe: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[])

Ein Tupel der in das logische Register codierten Daten und die zusätzlichen Qubits, die für die Darstellung des-Syndroms verwendet werden.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. errorcorrection. logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
- [Microsoft. Quantum. errorcorrection. encodeindebitflipcode](xref:Microsoft.Quantum.ErrorCorrection.EncodeIntoBitFlipCode)
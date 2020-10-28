---
uid: Microsoft.Quantum.ErrorCorrection.DecodeFromFiveQubitCode
title: Decodefrommevequbitcode-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: DecodeFromFiveQubitCode
qsharp.summary: Decodes the ⟦5, 1, 3⟧ quantum code.
ms.openlocfilehash: 421da6296b604f30aefed58730091f64f19c3a61
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702539"
---
# <a name="decodefromfivequbitcode-operation"></a>Decodefrommevequbitcode-Vorgang

Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)

Paketen [](https://nuget.org/packages/)


Decodiert den ⟦ 5, 1, 3 ⟧ Quantum-Code.

```qsharp
operation DecodeFromFiveQubitCode (logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : (Qubit[], Qubit[])
```


## <a name="input"></a>Eingabe

### <a name="logicalregister--logicalregister"></a>logicalregister: [logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)

Ein Array von Qubits, das den logischen Zustand des codierten 5-Qubit-Codes darstellt.



## <a name="output--qubitqubit"></a>Ausgabe: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[])

Ein Qubit-Array der Länge 1, das den nicht codierten Zustand im ersten Parameter sowie zusätzliche Qubits im zweiten Parameter darstellt.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. errorcorrection. fvequbitcodeencoder](xref:Microsoft.Quantum.ErrorCorrection.FiveQubitCodeEncoder)
- [Microsoft. Quantum. errorcorrection. logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
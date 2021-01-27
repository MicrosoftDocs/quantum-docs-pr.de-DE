---
uid: Microsoft.Quantum.ErrorCorrection.DecodeFromFiveQubitCode
title: Decodefrommevequbitcode-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: DecodeFromFiveQubitCode
qsharp.summary: Decodes the ⟦5, 1, 3⟧ quantum code.
ms.openlocfilehash: 9b4580cb88f03a16e3c9c55511d0ec5968cc636f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853167"
---
# <a name="decodefromfivequbitcode-operation"></a>Decodefrommevequbitcode-Vorgang

Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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
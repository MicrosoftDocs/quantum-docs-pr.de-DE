---
uid: Microsoft.Quantum.ErrorCorrection.DecodeFromSteaneCode
title: Decodefromsteanäcode-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: DecodeFromSteaneCode
qsharp.summary: An inverse encoding operation that maps an unencoded quantum register to an encoded quantum register under the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: e6831a8630c0a80c2abe7c4a720263f0de03edc4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702516"
---
# <a name="decodefromsteanecode-operation"></a>Decodefromsteanäcode-Vorgang

Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)

Paketen [](https://nuget.org/packages/)


Ein umgekehrter Codierungs Vorgang, der ein uncodiertes Quantum-Register einem codierten Quantum-Register unter dem Quantum-Code ⟦ 7, 1, 3 ⟧ Steane zuordnet.

```qsharp
operation DecodeFromSteaneCode (logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister) : (Qubit[], Qubit[])
```


## <a name="input"></a>Eingabe

### <a name="logicalregister--logicalregister"></a>logicalregister: [logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)

Ein Array von Qubits, das den logischen Zustand des codierten 5-Qubit-Codes darstellt.



## <a name="output--qubitqubit"></a>Ausgabe: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[])

Ein Qubit-Array der Länge 1, das den nicht codierten Zustand im ersten Parameter sowie zusätzliche Qubits im zweiten Parameter darstellt.

## <a name="remarks"></a>Hinweise

Der ausgewählte Decoder verwendet die CSS-Code Eigenschaft des ⟦ 7, 1, 3 ⟧ Steane-Codes, d. h., er korrigiert X-Fehler und Z-Fehler separat. Eine Eigenschaft des Codes besteht darin, dass der Speicherort der x-und z-Korrektur, die angewendet werden soll, die 3-Bit-Codierung des x-bzw. z-syndrotes ist, wenn es sich um eine ganze Zahl handelt.

## <a name="references"></a>Referenzen

- D. Gottesman, "Stabilisator Codes und Quantum Error Korrektur", "Ph.D. Thesis, Caltech, 1997; https://arxiv.org/abs/quant-ph/9705052

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. errorcorrection. steanecodebug](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeEncoder)
- [Microsoft. Quantum. errorcorrection. steanecodecodecoder](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeDecoder)
- [Microsoft. Quantum. errorcorrection. logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX
title: Steanecoderecoveryx-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCodeRecoveryX
qsharp.summary: Decoder for the X-part of the stabilizer group of the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: c90eac291ebe718d10377399184ad705bb51673e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98824697"
---
# <a name="steanecoderecoveryx-function"></a>Steanecoderecoveryx-Funktion

Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Decoder für den X-Teil der stabilikostabilisgruppe des ⟦ 7, 1, 3 ⟧ Steane Quantum-Codes.

```qsharp
function SteaneCodeRecoveryX (syndrome : Microsoft.Quantum.ErrorCorrection.Syndrome) : Pauli[]
```


## <a name="input"></a>Eingabe

### <a name="syndrome--syndrome"></a>-Syndrom:- [Syndrom](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)

Ein von der Messung des X-Teils des Stabilisators erteiles-Syndrom-Array.



## <a name="output--pauli"></a>Ausgabe: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]

Ein Array von Pauli-Vorgängen, das bei Anwendung auf das codierte Quantum-System den Fehler korrigiert, der entspricht `syndrome` .

## <a name="remarks"></a>Bemerkungen

Der ausgewählte Decoder verwendet die CSS-Code Eigenschaft des ⟦ 7, 1, 3 ⟧ Steane-Codes, d. h., er korrigiert X-Fehler und Z-Fehler separat. Eine Eigenschaft des Codes besteht darin, dass der Speicherort der x-und z-Korrektur, die angewendet werden soll, die 3-Bit-Codierung des x-bzw. z-syndrotes ist, wenn es sich um eine ganze Zahl handelt.

## <a name="references"></a>References

- D: Gottesman, "Stabilisator Codes und Quantum Error Korrektur", "Ph.D. Thesis, Caltech, 1997; https://arxiv.org/abs/quant-ph/9705052

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. errorcorrection. steanecoderecoveryx](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX)
- [Microsoft. Quantum. errorcorrection. steanecoderecoveryf](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryFns)
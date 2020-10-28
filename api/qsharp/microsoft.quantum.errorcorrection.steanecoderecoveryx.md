---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX
title: Steanecoderecoveryx-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCodeRecoveryX
qsharp.summary: Decoder for the X-part of the stabilizer group of the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: 0f6b987ca23bd9ff2076080d60f1ca756b36848e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702395"
---
# <a name="steanecoderecoveryx-function"></a>Steanecoderecoveryx-Funktion

Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)

Paketen [](https://nuget.org/packages/)


Decoder für den X-Teil der stabilikostabilisgruppe des ⟦ 7, 1, 3 ⟧ Steane Quantum-Codes.

```qsharp
function SteaneCodeRecoveryX (syndrome : Microsoft.Quantum.ErrorCorrection.Syndrome) : Pauli[]
```


## <a name="input"></a>Eingabe

### <a name="syndrome--syndrome"></a>-Syndrom:- [Syndrom](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)

Ein von der Messung des X-Teils des Stabilisators erteiles-Syndrom-Array.



## <a name="output--pauli"></a>Ausgabe: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]

Ein Array von Pauli-Vorgängen, das bei Anwendung auf das codierte Quantum-System den Fehler korrigiert, der entspricht `syndrome` .

## <a name="remarks"></a>Hinweise

Der ausgewählte Decoder verwendet die CSS-Code Eigenschaft des ⟦ 7, 1, 3 ⟧ Steane-Codes, d. h., er korrigiert X-Fehler und Z-Fehler separat. Eine Eigenschaft des Codes besteht darin, dass der Speicherort der x-und z-Korrektur, die angewendet werden soll, die 3-Bit-Codierung des x-bzw. z-syndrotes ist, wenn es sich um eine ganze Zahl handelt.

## <a name="references"></a>Referenzen

- D. Gottesman, "Stabilisator Codes und Quantum Error Korrektur", "Ph.D. Thesis, Caltech, 1997; https://arxiv.org/abs/quant-ph/9705052

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. errorcorrection. steanecoderecoveryx](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryX)
- [Microsoft. Quantum. errorcorrection. steanecoderecoveryf](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeRecoveryFns)
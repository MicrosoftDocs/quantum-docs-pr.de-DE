---
uid: Microsoft.Quantum.Canon.ApproximateQFT
title: Näherer Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApproximateQFT
qsharp.summary: Apply the Approximate Quantum Fourier Transform (AQFT) to a quantum register.
ms.openlocfilehash: ffa3a3737a43fbe6acc57700ae122a13586482e7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704514"
---
# <a name="approximateqft-operation"></a>Näherer Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Wenden Sie die ungefähre quantfourier Transform (aqft) auf ein Quantum-Register an.

```qsharp
operation ApproximateQFT (a : Int, qs : Microsoft.Quantum.Arithmetic.BigEndian) : Unit
```


## <a name="input"></a>Eingabe

### <a name="a--int"></a>a: [int](xref:microsoft.quantum.lang-ref.int)

Näherungs Parameter, der bestimmt, auf welcher Ebene die kontrollierten Z-Drehungen in der QFT-Verbindung gelöscht werden.

Der Näherungs Parameter a bestimmt die Bereinigungs Ebene der Z-Drehungen, d. h. a ∈ {0.. n} und alle Z-Drehungen 2D/2K, wobei k>a aus der QFT-Leitung entfernt werden. Es ist bekannt, dass für k >= Protokoll. (n) + Protokoll Taste (1/1) + 3 eine Grenze gebunden werden kann | | QFT-aqft | |<.


### <a name="qs--bigendian"></a>QS: [bigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)

das Quantum-Register von n Qubits, auf das die ungefähre Quantum Fourier-Transformation angewendet wird.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Hinweise

Für aqft sind Z-Drehung-Gates im Format 2D/2K und Hadamard Gates erforderlich.

Es wird davon ausgegangen, dass die Eingabe und die Ausgabe in der Big-d-Codierung codiert werden.

## <a name="references"></a>Referenzen

- [*M. roetteler, Th. Beth* , Appl. Algebra eng. Commun. Co. 19 (3): 177-193 (2008)](http://doi.org/10.1007/s00200-008-0072-2)
- [*D. kopierungsarxiv* : quant-ph/0201067v1](https://arxiv.org/abs/quant-ph/0201067)